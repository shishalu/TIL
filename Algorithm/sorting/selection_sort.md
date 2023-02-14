# 선택 정렬

**주어진 자료들 중 가장 작은 값부터 앞에 위치한 값과 순차적으로 교환하여 정렬**

```py
def selection_sort(numbers):
    number_count = len(numbers)
    for i in range(number_count - 1):
        # min_value = numbers[i]
        min_index = i
        for j in range(i, number_count - 1):
            # if numbers[j + 1] < min_value:
            #     min_value = numbers[i + 1]
            if numbers[j + 1] < numbers[min_index]:
                min_index = j + 1
        # 가장 작은 값과 현재 위치 교환
        numbers[min_index], numbers[i] = numbers[i], numbers[min_index]

    # 반환
    return numbers
```