# 31 함수에서 재귀호출 사용하기

### 제귀호출이란
- 함수 안에서 함수 자기 자신을 호출하는 방식
  
- 예시 코드
```
def gello():
    print('Hello, world')
    hello()
hello()
결과
Hello, world
Hello, world
Hello, world
```
hello 안에서 다시 hello 함수를 호출하고 있습니다

이처럼 게속 반복하기에 팩토리얼도 구할 수 있습니다
- 예시 코드
```
 def factorial(n):
        if n == 1:
            return 1
        return n * factorial(n - 1)
    
print(factorial(5))
결과
120
```

## 심사문제: 재귀호출로 피보나치 수 구하기

### 1. 위치인수 코드 작성 규칙
- 정수 한 개로 입력
- 입력 값의 범위는 10~30
- 입력된 정수가 피보나치 수를 출력
- 피보나치는 0과 1로 시작
- 다음 피보나치의 수는 바로 앞의 두 피보나치 수의 합

### 2. 작성시 시행착오 
- 피보나치를 구현하는데 큰 어려움을 느낌
- n이 1과 같다고만 생각하여 답이 나오지 않음
- return n으로 뺏다가 함수끼리 빼기로 함

### 3. 실제 구현 내용
- 10~30까지 중 숫자 하나를 작성
- 그 작성한 수의 피보나치 수를 계산하여 출력

### 전체 코드 정리
```
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n - 2)

n = int(input())
print(fib(n))
```
