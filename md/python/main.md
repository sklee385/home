---
layout: default
---
## main
- 파이썬에는 따로 메인 함수가 없다
- if __name__ == '__main__': 를 사용해서     
    import 한 것인지 실행한 것인지 구분 지으면서 메인 함수를 대신한다

```
def main():
    print("메인함수")

if __name__ == '__main__':
    main()
```
