# 카운팅 정렬

**항목들의 순서를 결정하기 위해 집합에 각 항목이 몇 개씩 있는지 세는 정렬 방식**

```py
def counting_sort(numbers):
    k = 9
    counts = [0] * (k + 1)
    number_cnt = len(numbers)

    # counts 원소 채우기
    for i in range(number_cnt):
        counts[numbers[i]] += 1
    print(counts)

    # counts 누적합
    for i in range(len(counts) - 1):
        counts[i + 1] += counts[i]

    # 반환
    result = [0] * number_cnt
    for i in range(number_cnt - 1, -1, -1):
        counts[numbers[i]] -= 1
        result[counts[numbers[i]]] = numbers[i]

    return result
```