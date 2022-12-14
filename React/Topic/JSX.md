# JSX

#### React에서 사용하는 React 전용 HTML

* ES6 기반 JavaScript 언어의 확장 문법 
    * 그러나 JSX는 자바스크립트의 공식적인 문법이라고 할 수는 없다.

* 기존 HTML방식과 속성값의 대소문자 정도 차이 등을 제외하곤 거의 비슷하다. 
    * 자바스크립트에서 HTML을 작성하듯이 비슷하게 작성할 수 있도록 해 주는 것이 JSX의 가장 큰 장점이자, 이를 사용하는 이유이다.

* 브라우저에서 실행하기 전에 코드가 번들링되는 과정에서 바벨을 사용하여 일반 자바스크립트 형태의 코드로 변환된다.

### JSX 문법의 특징

* 여러 줄에 HTML을 작성하려면 HTML을 괄호 안에 넣으십시오.


* 컴포넌트에 여러 요소가 있다면 반드시 부모 요소 하나가 감싸는 형태여야 한다.
    * 리액트가 사용하는 Virtual DOM 방식에서는 컴포넌트 변화를 감지할 때 효율적으로 비교하고자 컴포넌트 내부는 하나의 DOM 트리 구조로 이루어져야 한다는 규칙이 있기 때문이다. 
   
* 자바스크립의 값을 {}를 이용해 JSX 안에서 렌더링

* JSX 내부의 자바스크립트 표현식 내에서 if문을 사용할 수 없어서, 조건부 연산자(삼항 연산자)를 사용한다.

* undefined를 렌더링하지 않아야 한다.
    * 이는 OR 연산자를 사용해 방지할 수 있다.
    * JSX 내부에서 undefined를 렌더링 하는 것은 에러가 나지 않는다.

* JSX는 XML 규칙을 따르므로 HTML 요소를 제대로 닫아야 한다.
    * HTML이 제대로 닫히지 않으면 JSX에서 오류가 발생.

* class속성은 HTML에서 많이 사용되는 속성이지만 JSX는 JavaScript로 렌더링되고 키워드 class는 JavaScript에서 예약어이므로 JSX에서는 사용할 수 없어 className를 대신 사용한다. 
    * JSX가 렌더링되면 className 속성을 class속성으로 변환합.

* 기존에 HTML에서 스타일을 지정할 때 background-color 와 같이 - 문자가 포함된 이름들을, JSX에서 사용할 때에는 -를 없애고 카멜 표기법으로 작성해야 한다.

* JSX 내에서 주석을 작성할 때에는 { /* … */ } 와 같은 형식으로 작성한다.
    * 시작 태그를 여러 줄로 작성 시, 그 내부에서 // 를 사용하여 주석을 작성할 수도 있다.
