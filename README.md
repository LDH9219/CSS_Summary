# CSS_Summary

* 구조 : 웹 콘텐츠에 의미를 부여하고 구조를 형성 = HTML
* 표현 : 시각적인 디자인과 레이아웃 표현 = CSS
* 행위 : 모든 front-end 브라우저 상호작용을 담당 = JavaScript


## 1. CSS 선택자(Selector) 란?

### 1.1 Rule Set
![image](https://github.com/LDH9219/CSS_Summary/assets/62749021/47b4a955-63da-48f2-af4d-811d22c11d72)    
Rule Set은 HTML 페이지 안의 특정 요소들을 어떻게 렌더링(Rendering)할 것인지 브라우저에게 알려주는 css 문장이다.    
스타일 규칙이라고도 불리는 이 문장은 스타일에 관한 규칙들을 집합처럼 나타낸다.

이러한 문장들을 한 군데에 모으면 스타일 시트(Style Sheet)를 이루게 되어, 많은 수의 스타일 규칙들ㅇ르 관리하기 쉬워진다.

### 1.2 선택자(Selector)
Rule Set 제일 앞 부분의 선택자 요소이다. 왼쪽 중괄호 ```{```가 나오기 전의 부분 모두가 선택자이다.    
선택자는 Rule Set의 영향을 받는 HTML 페이지 안의 특정 element 들을 선택해서 선언 블록(Declaration Block)의 내용을 적용시킨다.

``` HTML
참고)
@media print { background-color:transparent;}

"@" 키워드로 시작하는 문장은 Rule Set이 아닌 At-Rule이기 때문에 위 문장에서의 중괄호 전 부분은 선택자가 아니다.
```

## 2. 선택자(Selector)의 종류
선택자의 종류와 css 레벨, 지원하지 않는 브라우저 버전에 대해서 설명한다.

### 2.1 전체 선택자(Universal Selector)
