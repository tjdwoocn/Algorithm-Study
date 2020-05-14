# [Python] A+B -7 (11021번)

### [문제]

두 정수 A와 B를 입력받은 다음, A+B를 출력하는 프로그램을 작성하시오.

### [입력/출력]

첫째 줄에 테스트 케이스의 개수 T가 주어진다.

각 테스트 케이스는 한 줄로 이루어져 있으며, 각 줄에 A와 B가 주어진다. (0 < A, B < 10)

```
각 테스트 케이스마다 "Case #x: "를 출력한 다음, A+B를 출력한다. 
테스트 케이스 번호는 1부터 시작한다.
3
1 1  --> Case #1: 2
2 3  --> Case #2: 5
4 3  --> Case #3: 7
```

### [코드]

```python
for i in range(int(input())):
	print('Case #'+str(i+1)+': ', eval('+'.join(input().split())))

or

for i in range(int(input())):
  print("Case #%d: %d"%(i+1,sum(map(int,input().split()))))
```

### [해설]

- 1.
    - range() 함수로 입력받은 값 만큼 loop
    - str 중간에 바꿔줘야 하는 Numbering 값 추가
    - eval() 함수로 입력되는 두 값 더해주고 출력
- 2.
    - 위와 거의 동일, "%d %d" %(첫 %d 의 값, 둘째 %d 의 값) 의 방법으로 해당값 넣어주기
    - sum(map(()) 으로 입력받은 두 값을 더해주기

### [효율성]

- 메모리: 29056 KB
- 시간: 68 ms
- 코드길이: 75 B
- 숏코딩

```python
i=1;exec("print(f'Case #{i}:',eval('+'.join(input())));i+=1;"*int(input()))

or

for i in range(int(input())):
  print("Case #%d:"%-~i,sum(map(int,input().split())))
```