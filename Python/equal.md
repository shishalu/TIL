# == 과 is의 비교

- **==** 은 내용물의 값이 동일한지 비교
- **is** 는 메모리의 저장 위치가 동일한지 비교

예시)
```py
a = 'apple'
b = 'apple'
# 문자열은 변환 불가능(immutable)이므로 다른 변수이더라도
# 하나의 메모리에 저장된 문자열을 받아준다

c = a[:3] + 'e'
# 슬라이싱을 통한 깊은 복사로 새로운 영역에 새로문 문자열로 저장된다

print(a == b) # True
print(a is b) # True
print(a == c) # True
print(a is c) # False 
```