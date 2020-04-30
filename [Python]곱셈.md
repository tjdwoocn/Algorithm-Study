# [Python] 곱셈

### [문제]

(세 자리 수) × (세 자리 수)는 다음과 같은 과정을 통하여 이루어진다.

![https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png](https://www.acmicpc.net/upload/images/f5NhGHVLM4Ix74DtJrwfC97KepPl27s%20(1).png)

(1)과 (2)위치에 들어갈 세 자리 자연수가 주어질 때 (3), (4), (5), (6)위치에 들어갈 값을 구하는 프로그램을 작성하시오.

### [입력/출력]

첫째 줄에 (1)의 위치에 들어갈 세 자리 자연수가, 둘째 줄에 (2)의 위치에 들어갈 세자리 자연수가 주어진다.

```
***예제 입력***: 472, 385 
***예제 출력***: 2360
				3776
				1416
				181720
```

### [코드]

```python
a,b=int(input()),input()

for i in reversed(b):
    print(a*int(i))

print(a*int(b))
```

### [해설]

- 일단 a, b 값을 입력받음
    - 이때 input() 함수를 통해 들어오는 값은 str 값으로 들어옴
    - a 는 int 로 변환시켜주고, b 는 str 값 그대로
- for문을 통해 str 값인 b를 단일 숫자별로('3','8','5') 출력해줌
    - 이때 뒷 숫자부터 곱해주고 출력해주기 위해 reversed() 함수 사용해
    - int 타입인 a 와 곱해주기위해 i 값을 int 타입으로 변환 후 곱해주기
    - '5', '8', '3'의 순서로 a 와 곱한 결과 출력
- a 와 int 타입으로 변환한 b의 곱셈 값 출력

### [효율성]

- 메모리: 29056KB
- 시간: 60 ms
- 코드길이: 68 B
- 숏코딩

```python
a,b=int(input()),input()
print(*[a*int(p)for p in b][::-1],a*int(b))
```