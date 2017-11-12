---
layout: default 
---

## nginx 연동
1. nginx 설치 
    ```
    yum install -y nginx 
    ```
2. nginx.conf 설정 변경
    ```
    vi /etc/nginx/nginx.conf
    ```     

    server{ 아래 lkocation을 붙여 놓는다.}
    ```
    location / {
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
      proxy_set_header Host $http_host;
      proxy_set_header X-NginX-Proxy true;
      proxy_pass http://127.0.0.1:3000/;
      proxy_redirect off;
    }
    ```
3. nginx 재시작
    ```
    service nginx restart 
    ```
    