---
layout: single
title:  "그리디 문제: 볼링공 고르기"
---

# 나의 풀이

~~~python

n,m = map(int,input().split())
data = list(map(int,input().split()))
result = 0

for i in range(n):
  for j in range(i,n-1):
    if data[i] == data[j+1]:
      result += 0
    else:
      result += 1

print(result)
     
~~~

# 책(이것이 코딩테스트다) 풀이

~~~python
n,m = map(int,input().split())
data = list(map(int,input().split()))

array = [0] * 11
for x in data:
  array[x] += 1
  
result = 0

for i in range(1, m+1):
  n -= array[i]
  result += array[i] * n

print(result)
~~~

내가 짠 코드도 정상적으로 답이 출력된다.
하지만 나는 볼링공의 무게 변수인 m을 활용하지 못했다.
책의 풀이를 이해하고 더 효율적인 코드를 작성해야겠다..
