## string.upper()과 string.isupper()

### 1. upper()과 lower()
- string.upper()
문자열 전체 대문자 변환

- string.lower()
문자열 전체 소문자 변환

### 2. .isupper()과 .islower()

- string.isupper()
문자열에 대문자가 있는지 검사

```py
s1 = 'Algorithm'
s2 = s1.lower()

print('Q. {0}에 대문자가 있나요? A. {1}'.format(s1, s1.isupper())) 
# True
print('Q. {0}에 대문자가 있나요? A. {1}'.format(s2, s2.isupper())) 
# False
```

- string.islower()
문자열에 소문자가 있는지 검사

```py
s1 = 'Algorithm'
s2 = s1.upper()

print('Q. {0}에 대문자가 있나요? A. {1}'.format(s1, s1.islower())) 
# True
print('Q. {0}에 대문자가 있나요? A. {1}'.format(s2, s2.islower())) 
# False
```