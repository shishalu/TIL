## .format()과 %s, %d, %f

### 1. .format()
```py
print('{} {}'.format('1', 'two'))
# 인덱스 위치를 통해 순서변경도 가능
print('{1} {0}'.format('two''1'))
```

### 2. %s, %d, %f
```py
print('%s %s' % ('one', 'two'))
print('%d %d' % ('1', '2')) #digit
print('%f %f' % ('1', '2'))
```

## print(end=" ")와 print('')

### print(end=" ")
- for문을 진행할 경우, 해당 결괏값 출력을 다음줄로 넘기지 않고 그 줄에서 계속 출력
- end 매개변수에는 줄바꿈 문자(\n)가 디폴트로 설정되어 있다

### print(' ')
- for문을 진행할 경우, 해당 결괏값 출력을 다음줄로 넘겨준다

예시) 구구단
```py
for i in range(2, 10):
    for j in range(1, 10):
        print(i * j, end="")
    print('')

# 2 4 6 8 10 12 14 16 18
# 3 6 9 12 15 18 21 24 27
# ...
# 9 18 27 36 45 54 63 72 81
```