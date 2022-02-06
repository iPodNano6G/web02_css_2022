# web02_css_2022
## CSS의 도입
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
우선 순위는 기본 < 클래스 < id 순서이다.  
https://www.w3schools.com/cssref/css_selectors.asp  
