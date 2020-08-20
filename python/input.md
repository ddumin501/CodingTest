### 숫자를 입력 받는법 
- 입력예시
> 5
> 65 90 75 34 99
- 출력예시
> 99 90 75 65 34

```python
# 데이터의 개수 입력
n = int(input())
# 각 데이터를 공백으로 구분하여 입력
data = list(map(int,input().split()))

data.sort(reverse = True)
print(data)
```

```python
# n, m, k를 공백으로 구분하여 입력
n, m, k = map(int, input().split())

print(n, m, k)
```
입력이 많을 경우, input() 함수를 사용하면 동작 속도가 느려 시간 초과로 오답 판정 받을 수도있다.

이를 해결하기위하여
```python
imp
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTUzNjM5MDE4MiwtMTI4NjkxMjgxOV19
-->