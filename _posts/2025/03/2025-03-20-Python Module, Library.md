---
layout: single
title: '파이썬 모듈과 라이브러리'
categories: Python
tags:
  - Python
toc: true
---

# **모듈(Module)과 라이브러리(Library)의 개념과 차이**

**파이썬의 모듈(Module)과 라이브러리(Library)의 개념과 차이**에 대해 정리해보겠습니다.  
파이썬에서는 코드의 재사용성을 높이기 위해 다양한 모듈과 라이브러리를 활용합니다.

---

## **1. 모듈(Module)과 라이브러리(Library)의 차이점**

| 개념 | 설명 |
|------|------|
| **모듈(Module)** | `.py` 파일 하나 |
| **패키지(Package)** | 여러 모듈을 포함하는 디렉토리 (폴더) |
| **라이브러리(Library)** | 여러 패키지를 포함하는 대규모 코드 집합 |

|구분|모듈(Module)|라이브러리(Library)|
|---|---|---|
|**정의**|특정 기능을 포함하는 `.py` 파일|여러 모듈과 패키지를 모아둔 것|
|**구성 요소**|하나의 `.py` 파일 (함수, 클래스, 변수 포함)|여러 개의 모듈과 패키지를 포함|
|**예시**|`math.py`, `random.py`|NumPy, Pandas, Matplotlib|
|**사용 방식**|`import module_name`|`import library_name` (라이브러리는 패키지 형태로 제공)|
|**규모**|단일 기능 제공 (작음)|다양한 기능 포함 (크고 복잡함)|

---

## **2. 모듈(Module)이란?**

- **모듈(Module)**은 특정 기능을 포함하는 `.py` 파일
- 여러 함수와 클래스를 포함하여 특정 기능을 수행
- 모듈을 사용하면 코드의 **재사용성을 높이고**, 유지보수를 쉽게 할 수 있음

###  **모듈 사용 방법**

```python
import math  # math 모듈 불러오기

print(math.sqrt(16))  # 제곱근 계산 (출력: 4.0)
print(math.pi)  # 원주율 값 (출력: 3.141592...)
```

---

## **3. 라이브러리(Library)란?**

- **라이브러리(Library)**는 여러 개의 모듈(Module)과 패키지(Package)로 구성된 코드 모음
- 특정 기능을 수행하는 다양한 모듈을 모아둔 형태
- 라이브러리는 파이썬 표준 라이브러리(내장)와 외부 라이브러리(설치 필요)로 나뉨

###  **라이브러리 사용 방법**

```python
import numpy as np  # NumPy 라이브러리 불러오기

arr = np.array([1, 2, 3])
print(np.mean(arr))  # 평균값 계산
```

---

## **4. 패키지(Package)와의 관계**

- **패키지(Package)**는 여러 개의 모듈을 포함하는 폴더(디렉토리)입니다.
- 패키지는 모듈을 그룹화하여 체계적으로 관리하는 역할을 합니다.
- 패키지는 `__init__.py` 파일을 포함하여 여러 모듈을 묶어서 관리합니다.

###  **패키지 구조 예시**

```
mypackage/  
│── __init__.py  
│── module1.py  
│── module2.py  
```

###  **패키지 사용 예시**

```python
from mypackage import module1
print(module1.some_function())
```

---

## **5. 주요 내장 모듈과 메소드**

###  **(1) Math 모듈 (수학 연산)**

|메소드|설명|
|---|---|
|`math.sqrt(x)`|x의 제곱근 반환|
|`math.pow(x, y)`|x의 y승 반환|
|`math.factorial(n)`|n! (팩토리얼) 반환|
|`math.log(x, base)`|밑이 base인 로그 계산|

```python
import math
print(math.sqrt(16))  # 4.0
print(math.pow(2, 3))  # 8.0
print(math.factorial(5))  # 120
print(math.log(8, 2))  # 3.0
```

---

###  **(2) Random 모듈 (난수 생성)**

|메소드|설명|
|---|---|
|`random.randint(a, b)`|a~b 사이의 정수 난수 생성|
|`random.random()`|0~1 사이의 실수 난수 생성|
|`random.choice(list)`|리스트에서 랜덤 요소 선택|
|`random.shuffle(list)`|리스트 요소를 랜덤하게 섞음|

```python
import random
print(random.randint(1, 10))  # 1~10 사이 난수
print(random.random())  # 0~1 사이 실수 난수
print(random.choice(["apple", "banana", "cherry"]))  # 리스트에서 랜덤 선택
```

---

###  **(3) Datetime 모듈 (날짜 및 시간)**

|메소드|설명|
|---|---|
|`datetime.datetime.now()`|현재 날짜 및 시간 반환|
|`datetime.datetime.strptime(date_str, format)`|문자열을 날짜 객체로 변환|
|`datetime.datetime.strftime(format)`|날짜 객체를 문자열로 변환|

```python
import datetime

now = datetime.datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))  # 현재 날짜 및 시간 출력
```

---

## **6. 데이터 분석을 위한 주요 라이브러리**

###  **(1) NumPy (수학 연산)**

```python
import numpy as np
arr = np.array([1, 2, 3, 4])
print(np.mean(arr))  # 평균값
print(np.sum(arr))  # 합계
```

###  **(2) Pandas (데이터 분석)**

```python
import pandas as pd
df = pd.DataFrame({"이름": ["홍길동", "이순신"], "나이": [25, 30]})
print(df.head())
```

###  **(3) Matplotlib (데이터 시각화)**

```python
import matplotlib.pyplot as plt
x = [1, 2, 3]
y = [10, 20, 30]
plt.plot(x, y, marker="o")
plt.show()
```

---

## **7. 사용자 정의 모듈 만들기**

- 사용자가 직접 `.py` 파일을 만들어 함수나 변수를 정의하고, 다른 파일에서 가져올 수 있습니다.

### **1) 사용자 정의 모듈 생성 (`mymodule.py`)**

```python
# mymodule.py

def greet(name):
    return f"안녕하세요, {name}님!"
```

### **2) 다른 파일에서 사용자 정의 모듈 사용**

```python
import mymodule
print(mymodule.greet("철수"))  # 안녕하세요, 철수님!
```

---

## **8. 결론**

###  ✅ **모듈, 패키지, 라이브러리의 차이**

- **모듈(Module)**: `.py` 파일 하나 (함수 및 클래스를 포함)
- **패키지(Package)**: 여러 모듈을 포함하는 폴더 (`__init__.py` 포함)
- **라이브러리(Library)**: 여러 패키지와 모듈을 모은 큰 기능 집합

###  ✅ **모듈을 사용하면?**

- **코드의 재사용성이 증가**
- **파일 크기를 줄이고 유지보수가 쉬워짐**
- **필요한 기능을 모듈로 분리하여 관리 가능**

-> **모듈과 라이브러리를 잘 활용하면 더욱 효율적인 파이썬 프로그래밍이 가능**
