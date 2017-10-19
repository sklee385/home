---
layout: default
---
## 내장 모듈 getopt

```
#-i : 입력 파일 이름
#-o : 출력 파일 이름
#-c : 특정 조건을 수행하라는 옵션

python example.py -i inputname -o outputname -c
```
- 위와 같은 옵션을 처리해야하는 프로그램이라면 sys.argv[1:] 인자를 파싱해가며 처리해야 하는데     
    사용하기 많이 불편하다
- 이를 좀더 하기 편하게 하기 위해 나온게 getopt 함수

```
getopt(args, options[, long_options])
```

```
import

try:
    options, args = getopt.getopt(sys.argv[1:], 'e:m:f:' )
except:
    print("없는 옵션")
    sys.exit(1)

for opt, arg in options:
    if op == '-e':
        print(arg)
    ...    
```
