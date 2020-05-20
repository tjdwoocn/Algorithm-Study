# [Python] 더하기 사이클 (1110번)

### [문제]

0보다 크거나 같고, 99보다 작거나 같은 정수가 주어질 때 다음과 같은 연산을 할 수 있다. 먼저 주어진 수가 10보다 작다면 앞에 0을 붙여 두 자리 수로 만들고, 각 자리의 숫자를 더한다. 그 다음, 주어진 수의 가장 오른쪽 자리 수와 앞에서 구한 합의 가장 오른쪽 자리 수를 이어 붙이면 새로운 수를 만들 수 있다. 다음 예를 보자.

26부터 시작한다. 2+6 = 8이다. 새로운 수는 68이다. 6+8 = 14이다. 새로운 수는 84이다. 8+4 = 12이다. 새로운 수는 42이다. 4+2 = 6이다. 새로운 수는 26이다.

위의 예는 4번만에 원래 수로 돌아올 수 있다. 따라서 26의 사이클의 길이는 4이다.

N이 주어졌을 때, N의 사이클의 길이를 구하는 프로그램을 작성하시오.

### [입력/출력]

첫째 줄에 N이 주어진다. N은 0보다 크거나 같고, 99보다 작거나 같은 정수이다.

```
첫째 줄에 N의 사이클 길이를 출력한다.
26   4
55   3
1   60
```

### [코드]

```python
num = input()
check = num
n = 0
while True:
    if int(num) < 10:
        num = '0'+num
    temp = str(int(num[0])+int(num[1]))
    if int(temp) < 10:
        temp = '0' + temp
    new_num = num[1] + temp[1]
    num = new_num
    n += 1
    if new_num == check:
        break
print(n)

or

num = int(input())
check = num
new_num = 0
temp = 0
count = 0
while True:
    temp = num//10 + num%10
    new_num = (num%10)*10 + temp%10
    count += 1
    num = new_num
    if new_num == check:
        break
print(count)
```

### [해설]

### [효율성]

- 메모리: 29288KB
- 시간: 60 ms
- 코드길이: 71 B
- 숏코딩

```python
a=t=int(input());c=0
while(c<1)+a-t:t=t%10*10+t*11//10%10;c+=1
print(c)

or

a=b=int(input())
t=0
while (t<1)+a-b:
   a=a%10*10+(a%10+a//10)%10
   t+=1
print(t)
```