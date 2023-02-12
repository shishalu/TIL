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

## string.replace(old, new, [count])
- count의 값을 설정하지 않으면 문자열 전체를 의미하는 count = -1
- **문자열**에서만 사용가능, 튜플이나 리스트에서 사용할 경우 *Attribute Error* 발생

예시)

```py
b = 'bananabanananaba'
print(b.replace('banana', 'apple'))    # appleapplenaba
print(b.replace('banana', 'apple', 1)) # applebanananaba
print(b.replace('banana', 'apple', 2)) # appleapplenaba
```


## string.isalpha()
- 문자열의 구성이 모두 알파벳인지 확인한다

**string.isdigit()**
- 문자열의 구성이 모두 숫자인지 확인한다

**string.isalnum()**
- 문자열의 구성이 모두 알파벳 또는 숫자인지 확인한다