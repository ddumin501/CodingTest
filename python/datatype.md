## List

### 리스트 컴프리헨션
```python
# 1부터 9까지의 수의 제곱 값을 포함하는 리스트
array = [i*i for i in range(1,10)]
print(array)

# N X M 크기의 2차원 리스트 초기화
n = 3
m = 3
array = [[0]*m for _ in rang(n)]
print(array)
```
### 리스트 관련 기타 메서드
|함수명|사용법|기능|
|----------------|----------------|-------------------------------|-----------------------------|
|append()|변수명.append()|삽입
|sort()|변수명.sort()|정렬(오름차순)|
|sort()|변수명.sort(reverse=True)|정렬(내림차순) |  
|reverse()|변수명.reverse()|리스트 내 원소의 순서를 뒤집는다|
|insert()|변수명.insert(삽입할 위치 인덱스, 삽입할 값)|특정한 인덱스 위치에 삽입
|count()|변수명.count(특정 값)|특정한 값을 가지는 데이터 개수 세기|
|remove()|변수명.remove(특정 값)|특정값을 갖는 원소 제거(하나만 제거됨)|

remove할때, 특정값 가지는 모든 원소를 제거하는 방법
```python
a = [1, 2, 3, 4, 5, 5, 5]
remove_set = [3, 5]

result = [i for i in a if  
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTM5MDcwMzY3MywtNTM0NTEzMzAxXX0=
-->