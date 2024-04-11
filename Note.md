# 챕터1
### 1. 미니콘다 파이썬 버전 바꾸기  
1. 개요
   미니콘다를 다운로드 받으니 기본적으로 최신 버전인 3.12.2 버전이 다운로드 받아짐(24년 3월 기준)
   다음 블로그들 참고해서 해결했다.  
   (https://technical-support.tistory.com/85)  
   (https://sweetburble.tistory.com/33)  
   (https://velog.io/@dudrkdl777/Tip%EC%95%84%EB%82%98%EC%BD%98%EB%8B%A4-%ED%8C%8C%EC%9D%B4%EC%8D%AC-%EB%B2%84%EC%A0%84-%EB%B3%80%EA%B2%BD%ED%95%98%EA%B8%B0)
   (https://whdgus928.tistory.com/20)
2. 기타  
   \- 미니콘다 파이썬 버전 선택 시, 3.8.10 이렇게 할 수도, 3.8 이렇게 할 수도 있다.

### 2. 가상환경 선택
![1. VS CODE ipynb 파일의 셀에서 우측 상단 클릭](https://github.com/j6paro/Python_Fastline/assets/115641176/fccc0f8d-69db-4f22-93ff-9d3a99da91b1)
1. VS CODE ipynb 파일의 셀에서 우측 상단 클릭  
![2. 상단에 뜬 Python Environments... 클릭](https://github.com/j6paro/Python_Fastline/assets/115641176/1e117f13-6cb9-466b-a1e0-a2b3be914adf)
2. 상단에 뜬 Python Environments... 클릭
![3. 원하는 가상환경 선택](https://github.com/j6paro/Python_Fastline/assets/115641176/ab154750-9c33-44c5-a319-1ee351d02a80)
3. 원하는 가상환경 선택

# 챕터2  
### 1. 파이썬 포매터(Formatter)  
1. 개요  
   \- 띄어쓰기 이상하게 된 애들 같이 서식 이상한 것들을 자동으로 수정해준다.  
   \- 우클릭해서 셀 서식 누를 수도 있고(ipynb), format on save 설정해주면 ctrl s 로 저장해줄 때마다 올바른 서식으로 잘 바꿔준다.

### 2. 파이썬 문법의 핵심 요소들[2/4]  
1. 개요  
   \- id() 함수 : 객체의 주소를 반환하여 준다.  
   \- 0.2 * 0.2 의 출력값이 0.04가 아니라 끝에 1이 붙는 이유 : 컴퓨터는 실수를 다룰 때 이진수를 다룬다. 1/2, 1/4, 1/8 등의 조합으로 표현하기 때문

### 3. 변수와 동적 타이핑  
1. 개요
   \- 파이썬에서는 자료형에 따라 메모리의 값만 바꿔줄 수 있는 자료형과 바꿀 수 없게 막아 놓은 자료형으로 나뉜다.
   ![immutable vs mutable](https://github.com/j6paro/Python_Fastline/assets/115641176/43fced1c-b67e-4e11-8bf0-3df34c24be40)

### 4. 리스트  
1. NoneType
   \- append에 마우스 우클릭 -> 정의 보기 -> append 옆 None의 의미는 해당 method를 호출했을 때 나오는 게 None, 즉 없다는 의미이므로 받으려고 하지 말라는 것이다. append는 새로운 객체를 생성하지 않는다.  
2. 리스트의 복사  
   \- = : 복사한 새 리스트 내 원소 바꾸면 복사당한 리스트 원소도 바뀐다.  
   \- .copy() : 복사한 새 리스트 내 원소 바꾸면 복사당한 리스트 원소는 그대로. 하지만 리스트 내 리스트의 원소를 바꾸면 복사당한 리스트 원소도 바뀐다.  
   \- copy.deepcopy() : 복사한 새 리스트 내 리스트의 원소를 바꿔도 복사당한 리스트 내 리스트의 원소는 그대로

### 5. 튜플  
1. 튜플은 불변형으로 내부 구조가 리스트보다 좀 더 단순하다. 그래서 튜플이 리스트보다 메모리를 적게 차지한다.  
   \- sys 모듈의 getsizeof() 함수로 확인 가능하다.  
2. 튜플의 불변성 훼손  
```python
t = ([1], 2)
new_t = t
new_t[0][0] = 2
print(t[0][0])
```  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;\- 위 코드의 실행 결과는 2가 나온다.
