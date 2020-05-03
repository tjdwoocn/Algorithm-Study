# [Python] A*B, A/B

### [문제]

두 정수 A와 B를 입력받은 다음, A*B를 출력하는 프로그램을 작성하시오.

```
A*B
첫째 줄에 A와 B가 주어진다. (0 < A, B < 10)
첫째 줄에 A*B를 출력한다. (1과 2가 입력될때 2이 출력되도록)

A/B
첫째 줄에 A/B를 출력한다. 
실제 정답과 출력값의 절대오차 또는 상대오차가 10-9 이하이면 정답이다.
1, 3 ==> 0.3333333333
```

### [코드]

```python
A, B = map(int, input().split())
print(A*B)

a,b,c=input();print(int(a)/(int(c))
```

### [해설]

- 이전과 동일

### [효율성]

- 메모리: 29160KB
- 시간: 64ms
- 코드길이: 34B
- 숏코딩

```python
a,b,c=input();print(int(a)*int(c))

print(eval('/'.join(input().split())))
```