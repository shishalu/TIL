# Dictionary 자료형

## Dictionary comprehension

### 1. enumerate()를 활용

```py
fruit_basket = ['apple', 'banana', 'watermelon', 'grape']
fruit_dic = {key : value for key, value in enumerate(fruit_basket)}
print(fruit_dic)

# {0: 'apple', 1: 'banana', 2: 'watermelon', 3: 'grape'}
```

### 2. zip()을 활용
```py
fruit_basket = ['apple', 'banana', 'watermelon', 'grape']
names = ['Andy', 'Kelly', 'Billie', 'Tony']
friend_dic = {name : fruit for name, fruit in zip(names, fruit_basket)}
print(friend_dic)

# {'Andy': 'apple', 'Kelly': 'banana', 'Billie': 'watermelon', 'Tony': 'grape'}
```

## value값 검색하기

### **dict[key]** 와 **dict.get(key)**
- **dict[key]**는 딕셔너리에 없는 key값이 주어졌을 때 오류 발생
- **dict.get[key]**는 딕셔너리에 없는 key값이 주어졌을 때 None을 리턴

```py
friend = {'Andy': 'apple', 'Kelly': 'banana', 'Billie': 'watermelon', 'Tony': 'grape'}

print(friend['Andy'])       # apple   
print(friend.get('Andy'))   # apple

print(friend['Hi'])         # KeyError 발생
print(friend.get('Hi'))     # None
```

## Counter()

