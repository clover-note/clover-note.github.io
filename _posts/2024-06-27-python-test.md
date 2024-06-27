```python
print("파이썬 수업 중")
```

    파이썬 수업 중



```python
print("2021-04-18")
```

    2021-04-18


# 파이썬 데이터 타입

정수, 실수, 문자열

# 변수 bind

a = 3 (가리키다-> 바인딩 binding)


```python
아이스크림 = 3
```


```python
id(아이스크림) #id(변수명) : 변수가 가리키는 메모리 주소값 출력 
```




    4307938472




```python
과자 = 1500
아이스크림 = 1000
```


```python
총금액 = 과자*5 + 아이스크림*7
```


```python
print(총금액)
```


```python
달러 = 1280
```


```python
총평가 = 900*달러
```


```python
print(총평가)
```

    1152000


# 개행문자와 탭
\n 줄바꿈
\t 탭

# 문자열 
### 1. indexing : 한글자 가져오기 
0부터 n까지/ 역순(마지막 문자)으로 하면 음수로 부르기(-1부터)
### 2. slicing : 여러글자 가져오기
범위 [시작인덱스:끝인덱스] 실제 부를때는 끝 -1로 불러짐



```python
lang = "Python3"
```


```python
type(lang)
```




    str




```python
id(lang)
```




    4444605744




```python
lang[0]
```




    'P'




```python
lang[1:3]
```




    'yt'




```python
lang[-1:] #끝인덱스 생략시 문자열 끝으로 간주
```




    '3'




```python
lang[:3] #시작인덱스 생략시 0으로 간주
```




    'Pyt'




```python
lang = "Python3"
```


```python
name = lang[:6]
```


```python
version = lang[-1:]
```


```python
print(name,version) #출력시 ,는 이어서 출력
```

    Python 3



```python
주민등록번호 = "801230-1062221"
```


```python
연월일 = 주민등록번호[:6]
```


```python
print(연월일)
```

    801230



```python
성별 = 주민등록번호[7]
```


```python
성별 = 주민등록번호[-7]
```


```python
print(성별)
```

    1



```python
ticker = "btc-krw"
```


```python
ticker.upper()
```




    'BTC-KRW'




```python
ticker.lower()
```




    'btc-krw'




```python
date = '2020/03/23'
```


```python
date.split('/')
```




    ['2020', '03', '23']



# 데이터 타입 immutable

int, float, str -> 변경할 수 없음 immutable


```python
name = "kakao"
```


```python
name[0]
```




    'k'




```python
name[0] = 'l'
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[9], line 1
    ----> 1 name[0] = 'l'


    TypeError: 'str' object does not support item assignment


# 문자열 변경
## 슬라이싱 / replace( ) -> 새로운 문자열 생성


```python
name = 'oyoung'
```


```python
new_name = 'd' + name
```


```python
new_name
```




    'doyoung'




```python
new_name2 = new_name.replace('d','j',1)
```


```python
new_name2
```




    'joyoung'




```python
len(new_name) #문자열 길이
```




    7




```python
code = "  005030 " #문자열 공백 제거 strip()
```


```python
code = code.strip()
```


```python
code # 초기 code 주소에 있던 값은 가비지 컬렉터가 바인딩 하지 않고 있는 값이라 제거
```




    '005030'




```python
close = "63,000,100" # 문자열 특정 문자 제거
```


```python
close1 = close.replace(",","")
```


```python
close2 = 630200
```


```python
type(close2)
```




    int



# int형 -> 문자 넣기


```python
format(close2, ",d")# int -> 특정 문자 삽입
```




    '630,200'



### 연습문제 1


```python
s = "Daum Kakao"
```


```python
s1 = s[5:] + " " +  s[:4]
```


```python
s1
```




    'Kakao Daum'



### 연습문제 2


```python
a = 'hello world'
```


```python
a = a.replace("helllo", "hi") # replace는 특정 문자만 변경
```


```python
a1 = 'hi'
```


```python
a = a1 + " " + a[6:]
```


```python
a
```




    'hi world'



### 연습문제 3


```python
date = "   2020/03/24"
```


```python
date = date.strip()
```


```python
date = date.replace("/","-")
```


```python
date
```




    '2020-03-24'



# 타입 변환


```python
a = "2"
```


```python
type(a)
```




    str




```python
숫자 = int(a)
```


```python
type(숫자)
```




    int




```python
year = 2024
```


```python
type(year)
```




    int




```python
문자 = str(year)
```


```python
type(문자)
```




    str



# 데이터타입 int flat str

# 자료구조 :  여러개의 데이터 타입을 담는 바구니(컬렉션)
### [리스트] : 순서0, 수정가능 [1,2,3]
### (튜플) : 순서0, 수정불가 (1,2,3)
### {딕셔너리} : 순서x, 수정가능 {label:값}


```python
아이스크림 = ['월드콘','메로나','스크류바']
```


```python
아이스크림[0]
```




    '월드콘'




```python
아이스크림[1]
```




    '메로나'




```python
아이스크림[2]
```




    '스크류바'



# 리스트 슬라이싱은 각각의 값 위에 있는게 아니고 범위 사이사이에 위치


```python
0| 월 1| 화 2| 수 3|
```


```python
print(아이스크림[0:3])
```

    ['월드콘', '메로나', '스크류바']



```python
print(아이스크림[1:2])
```

    ['메로나']


# 파이썬 리스트(수정, 추가, 삭제, 삽입) => 슬라이싱


```python
데이터타입은 immutable 수정불가하나
리스트는 수정가능
```


```python
아이스크림 = ["월드콘", "메로나", "빵빠레"]
```


```python
아이스크림[2] = "스크류바"
```


```python
print(아이스크림)
```

    ['월드콘', '메로나', '스크류바']


### 방법1


```python
data = ['a','b','c','d']
```


```python
data[0] = 'A'
```


```python
data
```




    ['A', 'b', 'c', 'd']



### 방법2


```python
data = ['a','b','c','d']
```


```python
data[0:2] = ['A','B']
```


```python
data
```




    ['A', 'B', 'c', 'd']



## list.append() 리스트 맨 뒤로 추가 <-> list.extend() 여러개 추가


```python
버킷리스트 = [] #빈 리스트 생성
```


```python
버킷리스트.append("파이썬 배우기") #리스트 요소 삽입
```


```python
버킷리스트.append("책집필")
```


```python
print(버킷리스트)
```

    ['파이썬 배우기', '책집필']


## list.insert(인덱스, 원소) 원하는 리스트 특정 위치(인덱스)에 삽입


```python
버킷리스트 = ['여행', '쇼핑', '에어비앤비']
```


```python
버킷리스트.insert(2, '부자되기')
```


```python
print(버킷리스트)
```

    ['여행', '쇼핑', '부자되기', '에어비앤비']


## del 리스트[인덱스] 특정 인덱스에 있는 원소 삭제


```python
del 버킷리스트[3]
```


```python
print(버킷리스트)
```

    ['여행', '쇼핑', '부자되기']


## list.extend() 리스트 확장


```python
num = [1,2,3]
```


```python
num.extend([4,5,6])
```


```python
# 리스트 함수는 리스트 본인 자체를 수정하기 때문에 
# print문에서 사용하면 none으로 출력-> 새로운 리스트를 생성하지 않음
```
