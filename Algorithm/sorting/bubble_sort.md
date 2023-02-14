# 버블 정렬

**인접한 두 개의 원소를 비교하며 자리를 계속 교환하는 방식**

```py
def bubble_sort(numbers):
    count = len(numbers)
    for i in range(count - 1):
        for j in range(count - 1):
            if numbers[j] > numbers[j + 1]:
                # 교환
                numbers[j], numbers[j + 1] = numbers[j + 1], numbers[j]
    return numbers
```