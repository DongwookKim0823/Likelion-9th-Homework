# < CSS >

## 1. CSS 기초

* CSS란 Cascading Style Sheets의 약자로 웹 페이지에 관한 다양한 스타일 들을 정의(스타일 담당)  

* 선택자(Selector) : 스타일을 적용하고자 하는 HTML 요소를 선택하는 역할  

* 속성(Property) : 지정할 스타일의 속성명에 해당. "속성:값;"이 한 단위. ;(세미콜론)을 이용하여 구분  

* 값(Value) : 키워드나 특정 단위를 이용하여 원하는 스타일을 적용. 속성(Property)와 쌍을 이룸  

* 선택자 뒤에 중괄호 안에 있는 블럭을 선언 블럭이라 칭함. 선언 블럭 내의 "속성:값;" 한쌍을 선언(Declaration)이라 부름  

* CSS를 HTML에 적용하는 방법  
  * Link style : HTML에 외부에 있는 CSS파일을 불러옴  
  * Embedding style : HTML의 ```<head>```에 ```<style>```를 이용하여 CSS를 작성  
  * Inline style : HTML요소에 직접 style 속성(Attributes)을 이용하여 CSS를 작성  

<br><br>
## 2. 선택자

* 선택자(Selector) : 스타일을 적용하고자 하는 HTML 요소를 선택하는 역할  

* 여러 개의 선택자를 ,(콤마)를 이용하여 스타일을 한번에 지정 가능  

* 단순 선택자(head 태그 내에 ```<style></style>``` 태그 사이에 작성)  

  * 타입 선택자(Type Selector) : 해당 태그를 가지는 모든 요소에 스타일 적용  
  * 아이디 선택자(Id Selector) : Id로 스타일을 적용. 해당 Id 하나에 적용(아이디는 ```<p id="지정아이디"></p>```처럼 사용)  
    * head 태그 내에 ```<style></style>``` 태그 사이에 ```#지정아이디 {속성:값;}``` 형식으로 작성  
  * 클래스 선택자(Class Selector) : 클래스 이름으로 스타일을 적용. 같은 클래스 이름이면 모두 적용  
    * ```<p class="클래스명"></p>```와 같이 태그 내에 클래스 지정을 한 뒤, head태그의 style태그 내에 ```.클래스명 {속성:값;}``` 형식으로 작성  
  * 전체 선택자(Universal Selector) : 모든 요소에 스타일을 적용. 모든 요소에 적용하기 때문에 속도 저하 가능성 있음. ```* {속성:값;}```와 같이 사용  
  * 속성 선택자(Attribute Selector) : 특정 속성을 소유하는 모든 요소에 스타일을 적용. ```선택자[속성명="속성값"] {속성:값;}```와 같이 사용  
  * 복합 선택자  
    * 자식 선택자(Child Selector) : 선택자A의 모든 자식 중 선택자B와 일치하는 요소 선택. ```선택자A>선택자B {속성:값;}``` 처럼 사용  
    * 후손 선택자(Descendant Selector) : 선택자A의 모든 후손 중 선택자B와 일치하는 요소 선택. ```선택자A 선택자B {속성:값;}```처럼 사용  
  * pseudo 클래스 선택자 : 요소의 특별한 상태를 지정할 때 씀  
    * ```선택자:link {속성:값;}``` : 방문하지 않은 링크일 경우  
    * ```선택자:visited {속성:값;}``` : 방문한 링크일 경우  
    * ```선택자:hover {속성:값;}``` : 요소에 마우스가 올라와 있을 경우  

<br><br>
## 3. 값, 단위, 색

* 속성에는 color, background-color, font-size, height, width 등이 있음  

* 값의 단위 중 숫자 값은 너비, 높이, 글자 크기 등을 조절하기 위해 자주 사용  

* 숫자 값의 단위  
  * px : 픽셀 1개의 크기(절대적인 길이), 참고로 웹브라우저의 기본 픽셀 크기는 16px임  
  * em : 현재 스타일이 지정된 요소의 font-size기준(상대적인 길이)  
  * rem : 최상위 요소(html문서에서 최상위 문서는 html태그)의 font-size기준(상대적인 길이). 또한 em보단 rem을 선호하자  

* 1em(1rem)의 크기 : 기준 font-size * 1em(1rem)  

* %(퍼센트) : 상대 길이, 보통 이미지나 레이아웃의 너비나 높이를 지정할 때 씀  

* 색을 표현하는 방법
  * hex code : #000000 (뒤에 추가적인 숫자로 밝기 조절 가능)
  * rgb : rgb(0,0,0) (뒤에 알파 값(0~1.0)을 추가하여 밝기 조절 가능-rgba(0,0,0,0))

<br><br>
## 4. 텍스트와 관련된 프로퍼티

* font-family 속성 : 값을 여러개로 주고, 첫번 째 폰트가 유저 인터페이스에서 적용시키지 못할 폰트이면 두번 째 폰트를 적용시키는 방식. 마지막엔 일반 글꼴을 두어야 함  

* 웹 폰트 : 구글 폰트와 같은 사이트에서 링크를 통해 폰트를 불러오는 방식으로, 링크 태그를 이용하는 방식과 CSS의 "속성:값" 방식으로 설정 가능  

* font-style 속성 : normal, italic, oblique 등이 존재  

* font-weight 속성 : 굵기 조절. bold, 100, ... ,400(normal), ... ,700(bold), ... ,900  

* font 속성 하나로 font-family, font-style, font-weight, font-size 모두 설정 가능  

* text-align : 부모요소를 기준으로 텍스트를 좌(left), 우(right), 중앙(center) 정렬함  

* line-height : 문장 사이의 간격을 조정함. 값은 24px, 2(기본 폰트 사이즈는 16px이므로 32px이 됨)처럼 사용  

* letter-spacing : 글자와 글자 사이의 간격을 조정함, 자간(값은 픽셀단위로 줌)  

* text-indent : 문단의 시작부에 들여쓰기를 함(값은 픽셀단위로 줌)  

<br><br>
## 5. 박스 모델

* HTML의 모든 요소는 상자(BOX)형태를 가진다  

* Box Model의 구성요소에는 내용(Content), 마진(Margin), 경계선(Border), 패딩(Padding)  

* 내용(Content)은 width와 height를 사용하여 표현  

* 경계선(Border)의 표현 방법
  * border-style : dashed solid dotted double; (지정 개수가 4개면 순서대로 시계방향으로 지정. 개수에 따라 지정 위치 바뀜. 아래 것들도 같음)
  * border-width : 6px;
  * border-color : red blue yellow green;
  * border-radius : 반지름 길이px; (개수 지정, 타원형 지정, 원하는 위치 지정, '/' 이용하여 각 모서리 지정 가능)

* border : 4px solid red; 와 같이 한번에 표현 가능  

* border 내부 여백을 Padding이라 하고, 외부 여백을 Margin이라 함  

* padding : 20px; 처럼 사용  

* margin : 20px; 처럼 사용(위, 아래 다른 요소에서 마진을 적용하면 두 마진이 공존하지 않고 큰 쪽 마진을 따라감 - 마진 상쇄(Margin Collapse))  

* box-sizing는 box의 기본 크기를 정하는 속성으로 box-sizing : content-box;(default값) , box-sizing : border-box; 처럼 사용 

<br><br>
## 6. 위치와 관련된 프로퍼티[1]

* display 속성 : 요소가 보여지는 방식을 지정  
  * display : block; - 항상 새로운 줄에서 시작하며, width 100%가 기본값. width, height, margin, padding 가능
  * display : inline; - 새로운 줄에서 시작하지 않으며, 요소의 content 크기 만큼의 width를 가짐. width, height, margin-top, margin-bottom 불가능
  * display : inline-block; 기본적인 쓰임은 inline과 동일. width, height, margin-top, margin-bottom 가능
  * display : none; 해당 요소가 디스플레이에 보이지 않음

* position 속성 : 요소의 위치를 정의
  * position : static; - 기본값, 좌표 프로퍼티를 쓸 수 없음
  * position : relative; - 상대 위치, 기본 위치를 기준으로 좌표를 사용함
  * position : absolute; - 부모나 조상 중 relative, absolute, fixed가 선언된 곳을 기준으로 좌표 프로퍼티 적용
  * position : fixed; - fixed는 보이는 화면을 기준으로 좌표 프로퍼티를 이용하여 위치를 고정

* z-index 속성 : 숫자값이 클 수록 전면에 출현하게 됨  

<br><br>
## 7. 위치와 관련된 프로퍼티[2]

* display방식과 positon방식은 어렵고 까다로워서 이를 대체하기 위한 flexbox를 주로 사용. 정렬을 쉽게 할 수 있음  

* flexbox
  * 정렬하고자 하는 부모 요소에 display : flex; 추가  

  * flex container(부모 요소)
    * flex-direction : flex 컨테이너 안의 item들의 방향을 정함.(default는 row;) 값으론 row; row-reverse; column; column-reverse; 가 있음
    * flex-wrap : flex 아이템이 flex 컨테이너를 벗어 났을 때 줄을 바꾸는 속성.(default는 nowrap;) nowrap; wrap; 가 있음
    * flex-flow : flex-direction과 flex-wrap 두가지 동시에 적용 가능. row wrap; 처럼 사용
    * justify-content : flex-direction으로 정해진 방향을 기준으로, 수평으로 item을 정렬하는 방법을 정함. flex-start;(왼쪽 정렬, 기본값), conter;(가운데 정렬), flex-end;(오른쪽 정렬), space-between;(시작과 끝을 기준으로 동일한 간격으로 정렬), space-around;(시작과 끝의 양쪽 여백이 있고, 모두 같은 간격으로 정렬)
    * align-items : flex-direction으로 정해진 방향을 기준으로, 수직으로 item을 정렬하는 방법을 정함. stretch;(기본값, 모든 요소 길이를 맞춰서 정렬), flex-start;(위로 정렬), flex-end;(아래로 정렬), conter;(가운데 정렬), baseline;(요소의 글꼴 기준선을 기준으로 정렬)
    * align-content : flex-direction으로 정해진 방향을 기준으로, 수직으로 __여러 줄__인 item을 정렬하는 방법을 정함. stretch;(기본값, 모든 요소 길이를 맞춰서 정렬), flex-start;(위로 정렬), flex-end;(아래로 정렬), center;(가운데 정렬), space-between;(위, 아래를 기준으로 동일한 간격으로 정렬), space-around;(위, 아래의 양끝 여백이 있고, 모두 같은 간격으로 정렬)
  * flex item(자식 요소)
    * flex-grow : flex 아이템의 확장과 관련된 속성, 숫자가 큰쪽이 더 커짐. 0이 기본
    * flex-shrink : flex 아이템의 축소와 관련된 속성, 숫자가 큰쪽이 더 작아짐. 1이 기본
    * flex-basis : flex 아이템의 기본 크기를 결정함, 기본 auto. px이나 %와 같은 단위의 값을 가짐
    * flex : flex-grow, flex-shrink, flex-basis의 축약형

<br><br>
## 8. 상속과 우선순위

* 모든 CSS 프로퍼티가 상속되는 것은 아님  

* 상속이 되지 않는 프로퍼티가 상속되길 원한다면 margin: inherit;을 추가  

* CSS 적용 우선순위 규칙
  * 중요도 : CSS가 어디에 선언되었는지에 따라 우선순위 바뀜
    * ```<head>```태그 내의 ```<style>```태그
    * ```<head>```태그 내의 ```<style>```태그 내의 ```@import```문
    *  ```<link>```태그로 연결된 CSS
    *  ```<link>```태그로 연결된 CSS 내의 ```@import```
    * 문브라우저 디폴트 스타일시트
  * 명시도
    * ```!important```
    * 인라인 스타일(inline style)
    * 아이디 선택자(id selector)
    * 클래스, 속성, 가상클래스 선택자(class, attribute, pseudo class selector)
    * 태그 선택자(type selector)
    * 전체 선택자(universal selector)
    * 상속(inherit)
  * 선언 순서 : 나중에 선언된 스타일이 우선 적용