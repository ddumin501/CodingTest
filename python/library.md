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

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc2MTEyMjg3NSwzNzUwMDMyNzFdfQ==
-->