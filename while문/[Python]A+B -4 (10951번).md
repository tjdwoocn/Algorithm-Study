# [Python] A+B -4 (10951번)

### [문제]

두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### [입력/출력]

입력은 여러 개의 테스트 케이스로 이루어져 있다.

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

```
각 테스트 케이스마다 A+B를 출력한다.
1 1    2
2 3    5
3 4    7
9 8   17
5 2    7
```

### [코드]

```python
while True:
    try:
        a,b = map(int, input().split())
    except:
        break
    print(a+b)

or

# 정석이라고 함
import sys
 
for line in sys.stdin:
    a, b = map(int, line.split())
    print(a + b)
```

### [해설]

- 1.
    - 몇개의 테스트 케이스가 주어지는지 정해져 있지 않은경우 EOF까지 받아야 함
        - EOF (End-of-File): Computer os가 데이터 소스로부터 읽어올 데이터가 더이상 없는 상황
    - while True로 반복 걸어주고 (아래의 조건들에서 False값이 나오기 전까진 계속 반복)
    - try-except로 예외/오류 처리를 해줍니다
        - 우선, try로 조건이 들어오고, 해당 조건이 try 내부 코드에 적합하면 코드 실행, 아니면 except 쪽으로 이동
        - 조건에 맞지 않는 상황이면 except로 간 뒤 코드 실행 (여기선 break)(어떤 오류가 발생했는지 출력하는 것도 있음)
    - try 내부 코드를 거친 결과값을 가지고 print(a+b) 실행
- 2.
    - sys를 import 해주고
    - sys.stdin 으로 입력받은 각 line의 값들을
    - a와 b로 나눠주고 a+b 값을 출력

### [효율성]

- 메모리: 29056KB
- 시간: 68 ms
- 코드길이: 56 B
- 숏코딩

```python
try:
 while 1:print(eval('+'.join(input())))
except:pass
```