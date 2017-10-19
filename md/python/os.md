---
layout: default
---
## 내장 모듈 os
```
import os
# 현재 디렉토리 리스트
os.listdir()
# c: 리스트
os.listdir("c:")

# 사용자 홈디렉토리 위치
os.path.expanduser("~")
# 사용자 홈 디렉토리 리스트
os.listdir(os.path.expanduser("~"))

# 디렉토리 생성
# 상위 디렉토리가 없으면 생성
os.makedirs("c:/Users/adsound/1/2/3/4")
# 홈디렉토리 밑에 파일 생성
os.makedirs(os.path.expanduser("~")+"/123/123")
# 비어있지 않는 디렉토리 삭제
os.rmdir(os.path.expanduser("~")+"/123")

# 현재 디렉토리 위치
os.getcwd()
# 현재 디렉토리 이름
os.path.basename()
# 현재 디렉토리 파일명
os.path.basename(os.getcwd())

# os commend 실행
os.system("ls")
```
