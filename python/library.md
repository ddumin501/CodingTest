## itertools
파이썬에서 반복되는 데이터를 처리하는 기능을 포함하고 있는 라이브러리이다.

이 중, 가장 유용하게 사용할 수 있는 클래스는 **permutations(순열)**, **combination(조합)** 이다.

```python
from itertools import permutations

data = ['A', 'B', 'C'] #데이터 준비

result = list(permutations(data,3)) #모든 순열 구하기
print(result)

#출력 
#[('A', 'B', 'C'), ('A', 'C', 'B'), ('B', 'A', 'C'), ('B', 'C', 'A'), ('C', 'A', 'B'), ('C', 'B', 'A')]
```

```python
from itertools import combinations

data = ['A', 'B', 'C'] #데이터 준비

result = list(combinations(data,2)) #2개를 뽑는 모든 조합
print(result)

#출력
#[('A', 'B'), ('A', 'C'), ('B', 'C')]
```

그 외 중복을 허용하는 
**product**(중복순열)
```
[('A', 'A'), ('A', 'B'), ('A', 'C'), ('B', 'A'), ('B', 'B'), ('B', 'C'), ('C', 'A'), ('C', 'B')('C', 'C')]
```
**combinations_with_replacement** (중복조합) 이 있다.
```
[('A', 'A'), ('A', 'B'), ('A', 'C'), ('B', 'B'),('B', 'C'),('C', 'C')]
```
## heapq
우선순위 큐 기능을 구현하고자 할 때 사용.
코딩테스트 환경에서는 보통 heapq가 PriorityQueue 라이브러리보다 더 빠르게 동작한다.
파이썬의 힙은 최소 힙(Min Heap)으로 구성되어 있다.
```python
#Min Heap
import heapq

def heapsort(iterable):
    h = []
    result = []
    # 모든 원소를 차례대로 힙에 삽입
    for value in iterable:
        heapq.heappush(h, value)
    # 힙에 삽입된 모든 원소를 차례대로 꺼내어 담기
    for i in range(len(h)):
        result.append(heapq.heappop(h))
    return result

result = heapsort([1,3,5,7,9,2,4,6,8,0])
print(result)
```
```python
#Max Heap
import heapq

def heapsort(iterable):
    h = []
    result = []
    # 모든 원소를 차례대로 힙에 삽입
    for value in iterable:
        heapq.heappush(h, -value)
    # 힙에 삽입된 모든 원소를 차례대로 꺼내어 담기
    for i in range(len(h)):
        result.append(-heapq.heappop(h))
    return result

result = heapsort([1,3,5,7,9,2,4,6,8,0])
print(result)
```

## bisect
이진 탐색을 쉽게 구현할 수 있도록 하는 라이브러리.

- bisect_left(a, x) :정렬된 순서를 유지하면서 리스트 a 에 데이터 x를 삽입할 가장 왼쪽 인덱스를 찾는 메서드
-  bisect_right(a, x) :정렬된 순서를 유지하면서 리스트 a 에 데이터 x를 삽입할 가장 오른쪽 인덱스를 찾는 메서드

```python
from bisect import bisect_left, bisect_right

a = [1, 2, 4, 4, 8]
x = 4

print(bisect_left(a,x))
print(bisect_right(a,x))

# 2
# 4
```
이를 활용하여 정렬된 리스트에서 값이 특정범위에 속하는 원소의 개수를 구할 수 있다.

```python
from bisect import bisect_left, bisect_right

#값이 [left_value, right_value]인 데이터의 개수를 반환하는 함수
def count_by_range(a, left_value, right_value):
	left_index = bisect_left(a,left_value)
	right_index = bisect_right(a,right_value)
	return right_index - left_index

#리스트 선언
a = [1, 2, 3, 3, 3, 3, 4, 4, 8, 9]

#값이 4인 데이터 개수 출력
print(count_by_range(a,4,4))
#값이[-1, 3] 범위에 있는 데이터 개수 출력
print(count_by_range(a,-1,3))

# 2
# 6
```

## collections
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTI3OTI4MDk4NCwtMTMzMDQwMTM5LDE3MT
I5OTc3ODYsLTY1MTkyMDQ2LC03NjExMjI4NzUsMzc1MDAzMjcx
XX0=
-->