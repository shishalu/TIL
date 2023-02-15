# enumerate()
- **리스트** 자료형에 사용 가능
- 인덱스 번호와 원소를 tuple 형태로 반환

```py
a = [1, 2, 3, 4, 5]

for idx, n in enumerate(a, start = 3):
    print(idx, n)

# start를 통해 시작 인덱스 변경
# 3 1
# 4 2
# 5 3
# 6 4
# 7 5
```
- 인덱스를 통해 리스트의 원소를 불러오기 보다, 원소 자체를 출력하는 것이 Python의 방식

### 이차원 리스트에서의 활용

```py
b = [[1, 2, 3],[6, 7, 8]]

for i, row in enumerate(b):
    for j, number in enumerate(row):
        print(i, j, number)

# 0 0 1
# 0 1 2
# 0 2 3
# 1 0 6
# 1 1 7
# 1 2 8

```

# items()
- **딕셔너리** 자료형에 사용 가능
- key와 value의 값을 tuple 형태로 반환

```py
dict_test = {'one':'apple', 'two':'banana', 'three':'watermelon'}

print(dict_test.items())

# dict_items([('one', 'apple'), ('two', 'banana'), ('three', 'watermelon')])