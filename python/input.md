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
n, m, k = map(int, input().split))
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbMjc5MzY1NzIzLC0xMjg2OTEyODE5XX0=
-->