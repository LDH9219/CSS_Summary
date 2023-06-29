# CSS_Summary

* 구조 : 웹 콘텐츠에 의미를 부여하고 구조를 형성 = HTML
* 표현 : 시각적인 디자인과 레이아웃 표현 = CSS
* 행위 : 모든 front-end 브라우저 상호작용을 담당 = JavaScript

***

## 1. CSS 선택자(Selector) 란?

### 1.1 Rule Set
![image](https://github.com/LDH9219/CSS_Summary/assets/62749021/47b4a955-63da-48f2-af4d-811d22c11d72)    
Rule Set은 HTML 페이지 안의 특정 요소들을 어떻게 렌더링(Rendering)할 것인지 브라우저에게 알려주는 css 문장이다.    
스타일 규칙이라고도 불리는 이 문장은 스타일에 관한 규칙들을 집합처럼 나타낸다.

이러한 문장들을 한 군데에 모으면 스타일 시트(Style Sheet)를 이루게 되어, 많은 수의 스타일 규칙들을 관리하기 쉬워진다.

### 1.2 선택자(Selector)
Rule Set 제일 앞 부분의 선택자 요소이다. 왼쪽 중괄호 ```{```가 나오기 전의 부분 모두가 선택자이다.    
선택자는 Rule Set의 영향을 받는 HTML 페이지 안의 특정 element 들을 선택해서 선언 블록(Declaration Block)의 내용을 적용시킨다.

```css
참고)
@media print { background-color:transparent;}

"@" 키워드로 시작하는 문장은 Rule Set이 아닌 At-Rule이기 때문에 위 문장에서의 중괄호 전 부분은 선택자가 아니다.
```

***

## 2. 선택자(Selector)의 종류
선택자의 종류와 css 레벨, 지원하지 않는 브라우저 버전에 대해서 설명한다.

### 2.1 전체 선택자(Universal Selector)
|패턴|의미|CSS LEVEL|미지원 브라우저|
|:------:|:---|:---:|:-----:|
| * |HTML 페이지 내부의 모든 태그를 선택합니다.|2| - |

**[예제] 전체 선택자**
```css
*{ margin: 0; text-decoration:none;}
```

**설명)**    
전체 선택자는 HTML 페이지 내부의 모든 요소(태그)에 같은 CSS 속성을 적용한다. 그렇기 때문에 보통 [예제] 처럼 ```margin```이나 ```padding``` 값을 초기화하는 등 기본값을 정해둘 때 사용한다.    
하지만 이를 자주 사용하면 문서안의 모든 요소를 읽어내려야 하기 때문에 페이지 로딩의 속도가 느려질 수 있으므로 자주 사용하지 않는 것이 좋다.

### 2.2 태그 선택자(Type Selector)
|패턴|의미|CSS LEVEL|미지원 브라우저|
|:------:|:---|:---:|:-----:|
| E |태그명이 E인 특정 태그를 선택합니다.|2| - |

**[예제] 태그 선택자**
```css
p{background:yellowgreen; color:darkgreen;}

<!--HTML-->
<p> 태그 선택자(Type Selector)</p>
<div> 태그 선택자(Type Selector)</div>
```

**설명)**    
태그 선택자는 HTML 요소를 직접 지칭하는 가장 간단한 선택자이다. [예제]를 보면 css에서 태그에 대한 스타일만 지정이 되어 있으므로, 태그에는 개발자가 지정해주는 스타일이 적용되지 않는다.
