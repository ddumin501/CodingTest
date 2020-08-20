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
|함수명|기능|
|----------------|-------------------------------|-----------------------------|
|변수명.append()|삽입
|변수명.sort()|정렬(오름차순) |
|sort(reverse=True)|정렬(내림차순) |  
|reverse()||
|insert()||
|count()||
|remove()||
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc1MzIxMDE1MywtNTM0NTEzMzAxXX0=
-->