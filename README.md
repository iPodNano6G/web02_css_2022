# web02_css_2022
## 0. CSS의 도입
인터넷이 대중적으로 변함에 따라, 사람들의 요구는 다양해지기 시작했다. 더 다양한 디자인과 기능을 원하게 된 것이다. 이를 추가하는 것은 쉽다. HTML 문법에 새로운 태그를 추가하면 된다. 하지만 이렇게 된다면 익히기 어렵고 방대한 문법이 만들어질것이 당연했다. 이를 피하기 위해 도입된 것이 CSS이다.
## 1. CSS의 기본을 알아보자
CSS를 적용하는 가장 쉬운 방법은 `<head></head>` 태그 안에 `<style><style>` 태그를 삽입하고, 값을 입력하는 것이다.  
`선택자 { (스타일 속성(property)) : (스타일 값) }` 형태로 이루어진다. CSS의 속성은 attribute가 아니고, property이다!  
ex ) `a { color : red; }`  
선택자를 제외한 나머지 부분은 직관적으로 유추할수 있다. 그런데 선택자는 무엇일까? 선택자는 말그대로 태그를 선택하는 역할을 한다. 선택자가 p라면 html 문서 내의 `<p>내용</p>`이 전부 영향을 받게 된다.  

기존에는 `<a href="1.html" ><font color="red">HTML</font></a>`처럼 `<font></font>`에 속성을 입력하였다.  
`<a href="2.html" style="color:red;text-decoration:underline">CSS</a>` CSS를 문서 전체가 아니라 특정 태그에만 적용하고 싶다면, 기존 태그에 style 속성을 적용하면 된다.

protery 참고 사이트

자주 사용하는 속성
https://velog.io/@bungouk6829/CSS-%EC%9E%90%EC%A3%BC-%EC%82%AC%EC%9A%A9%EB%90%98%EB%8A%94-%EC%86%8D%EC%84%B1

폰트 사이즈
https://careerkarma.com/blog/css-font-size/

## 2. 선택자
`a { }`인 경우에는 태그가 a인 경우에 적용된다.   
`.class`인 경우에는 태그의 속성에서 class가 `class="class"`인 경우에 적용된다. 하나의 태그가 여러개의 class를 가질 수 있고, 두 개의 구문이 다른 지시를 하고 있을 경우 아래에 있는것이 적용된다.  
`#id`인 경우에는 태그의 속성에서 id가 `id="id"`인 경우에 적용된다. 같은 id는 하나만 사용해야한다.  
우선 순위는 **기본 < 클래스 < id** 순서이다.  
https://www.w3schools.com/cssref/css_selectors.asp  
`,`를 사용해서 여러개의 선택자를 묶을수도 있다.  
`#grid ol` 선택자를 연달아 사용하면 왼쪽을 부모로 가지는 자식 태그에만 적용된다.


## 3. Box Model
### 3.1. Block and Inline 
Inline element는 Content만을 감싼다.  
Block element는 새로운 Line에서 시작하며, 해당 라인의 모든 너비를 차지한다.  
style tag에서 display property를 통해 설정할수 있다.

![이미지이름](boxmodel.gif)  
개발자 도구(F12) - 요소(Element)에서 페이지 내 객체들의 성분을 알 수 있다.

## 4. GRID
### 4.1. div,span 태그
디자인을 위해서만 사용되는 무의미한 태그  
div의 default는 block element,
span의 default는 inline element이다.

#### 4.2. grid
`display:grid;`  
`grid-template-columns: 150px 1fr;`  
해당 display property를 grid로 설정하고, 
`grid-template-"내용"`을 설정하면 된다.
value에 따라 크기가 정해진다. 예를 들어 `150px 1fr 1fr`이라면 150픽셀 고정에 오른쪽 두 칸은 1대 1 비율로 출력되게 된다.
### 4.3. 유용한 사이트
https://caniuse.com/  
grid는 최신 기능이기에 지원하지 않는 브라우저도 존재할수 있다. 해당 사이트에서 CSS, JS가 지원하는 기술과 지원하지 않는 기술을 확인할수 있다.

## 5. 반응형 디자인과 미디어 퀴리
웹 페이지의 크기에 따라 화면의 요소들이 다르게 표시되는 것이 반응형 디자인  
`@media(min-width:800px) {내용}` 해당 구문에 조건을 입력하면 조건에 따라 `내용`부분의 코드가 실행된다.