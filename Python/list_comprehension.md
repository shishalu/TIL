# List Comprehecsion
- 리스트를 **한줄로 짧게** 만들수 있는 문법
- 배열을 만들고 for문 안에서 각 원소의 값을 할당하는 과정

[(변수를 활용한 값) for (사용할 변수 이름) in (순회할 수 있는 값(iterable))]

## 문자열 활용

예시)
```py
morning = '아침이슬'
print([s * 2 for s in morning])

# ['아아', '침침', '이이', '슬슬']
```


## if 조건문을 활용한 필터링

예시) 1부터 20까지의 값 중 홀수만 원소로 갖는 리스트
```py
num_arr = [n for n in range(1, 21) if n % 2]
print(num_arr)

# [1, 3, 5, 7, 9, 11, 13, 15, 17, 19]
```

## list comprehension을 통해 AND 조건식 사용

예시) 1부터 20까지의 값 중 2의 배수이면서 5의 배수인 수만 원소로 갖는 리스트
```py
num_arr = [n for n in range(1, 21) if n % 2 == 0 if n % 5 == 0]
print(num_arr)
# [10, 20]
```

- and를 명시적으로 쓰면 안된다 (SyntaxError 발생)

## list comprehension을 통해 OR 조건식 사용

예시) 1부터 20까지의 값 중 2의 배수이거나 5의 배수인 수만 원소로 갖는 리스트
```py
num_arr = [n for n in range(1, 21) if n % 2 == 0 or n % 5 == 0]
print(num_arr)
# [2, 5, 6, 8, 10, 12, 14, 16, 18, 20]
```

- if 문을 여러개 사용하면 안된다 (or를 작성해야 한다)

## 2차원 매트릭스에서의 활용

예시)
```py
arr = [[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]]
num_arr = [n for row in arr for n in row]
print(num_arr)
# [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

**!!단순 데이터 조작과의 구분**

예시)
```py
arr = [[1, 2, 3], [4, 5, 6], [7, 8, 9], [10, 11, 12]]
num_arr = [[n ** 2 for n in row] for row in arr]
print(num_arr)
# [[1, 4, 9], [16, 25, 36], [49, 64, 81], [100, 121, 144]]
```
