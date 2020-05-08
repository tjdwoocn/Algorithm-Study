# [Python] 사분면 고르기

### [문제]

흔한 수학 문제 중 하나는 주어진 점이 어느 사분면에 속하는지 알아내는 것이다. 사분면은 아래 그림처럼 1부터 4까지 번호를 갖는다. "Quadrant n"은 "제n사분면"이라는 뜻이다.

![https://onlinejudgeimages.s3-ap-northeast-1.amazonaws.com/problem/14681/1.png](https://onlinejudgeimages.s3-ap-northeast-1.amazonaws.com/problem/14681/1.png)

예를 들어, 좌표가 (12, 5)인 점 A는 x좌표와 y좌표가 모두 양수이므로 제1사분면에 속한다. 점 B는 x좌표가 음수이고 y좌표가 양수이므로 제2사분면에 속한다.

점의 좌표를 입력받아 그 점이 어느 사분면에 속하는지 알아내는 프로그램을 작성하시오. 단, x좌표와 y좌표는 모두 양수나 음수라고 가정한다.

### [입력/출력]

첫 줄에는 정수 x가 주어진다. (−1000 ≤ x ≤ 1000; x ≠ 0) 다음 줄에는 정수 y가 주어진다. (−1000 ≤ y ≤ 1000; y ≠ 0)

```
점 (x, y)의 사분면 번호(1, 2, 3, 4 중 하나)를 출력한다.

예) 
12, 5  --> 1 
9, -13 --> 4
```

### [코드]

```python
x=int(input())
y=int(input())
print(1 if x>0 and y>0 else (2 if x<0 and y>0 else (3 if x<0 and y<0 else 4)))

or

print("3421"[(int(input())>0)+(int(input())>0)*2])
```

### [해설]

- 1번
    - 첫째줄과 두번째줄에서 x와 y 값을 입력받음
    - 셋째줄에서 한줄 중첩 조건문으로 각 x와 y의 값을 비교하여 해당되는 사분면을 구하고 결과값 출력
- 2번
    - int(True) =1, int(False) =0 을 이용
    - '3421': x와 y 모두 False 일때 = 0

                      x만 True 일때 = 1

                      y만 True 일때 = 1*2 = 2

                      x와 y 모두 True 일때 = 1+ (1*2) = 3

### [효율성]

- 메모리: 29284KB
- 시간: 60 ms
- 코드길이: 50 B
- 숏코딩

```python
print("3421"[(int(input())>0)+(int(input())>0)*2])

or

x = int(input()) < 0
y = int(input()) < 0
print((x^y) + 2*y + 1)

or

x=int(input())
y=int(input())
print((1 if y>0 else 4) if x>0 else (2 if y>0 else 3))
```