react를 배워야 하는 이유
1. 가장 많은 이용자 -  커뮤니티 활성화
2. 웹, 앱, 데스크탑앱 모두 만들 수 있다. - All In One

***컴포넌트**란 _UI 또는 기능을 부품화해서 재사용_ 가능하게 하는 것
기본적으로는 원본이 통제하고 원본만 변경하면 모두 적용 가능. 원하는 부분들은 따로 바꿀 수도 있다. 
➡️복사+붙여넣기와 다른 이유: 수정이 필요할 경우 모든 게시물 하나하나 수정.(비효율)
컴포넌트는 원본을 공유하고 있기 때문에 원본이 바뀌면 다 같이 바뀜.(원본이 통제하는 방식, 효율적)

부분 부분 작은 컴포넌트와 하나의 큰 페이지도 컴포넌트로 페이지 컴포넌트라고 하며
컴포넌트 안에 컴포넌트가 들어가는 것도 가능하다. 

컴포넌트는 두가지 유형이 있다.
![](https://velog.velcdn.com/images/ahk1106/post/44f05f58-b737-4e4d-91e2-15c6bffbe957/image.png)
-function이 하나의 컴포넌트이다 -> 함수형 컴포넌트
-함수형 컴포넌트 => 화살표 함수로 표현 가능 (코드길이가 짧아진다)
-클래스형과 함수형은 섞어 쓸 수 있다. 
-주로 함수형을 쓰지만 아직도 사용하는 곳이 있어 클래스형도 알아야 한다.
-클래스형을 함수형으로 변경 가능하다.

처음부터 쓰지 왜 이제서야 함수형을 쓰는 거야? 
이후에 use로 사용하는 기능(= hooks)이 생겼다. (리액트 업데이트)
**React-Hooks의 함수형 컴포넌트** :  _Hooks_는 함수형을 클래스형과 동일한 기능을 사용 가능하도록 만들어 준다.덕분에 함수도 컴포넌트 형태로 사용할 수 있게 되었다.
*Hooks란 **use**State, **use**Effect,... use로 시작하는 기능들

*state: 컴포넌트 전용 변수
*setstate: 변수 바꾸기(함수)
*useState: React component에서 사용하는 변수, State를  만들어준다.
useState라는 기능이 있어야 변수를 만들 수 있다.
? 변수는 let, const로 만드는 거 아니었어? 맞아 그런데 컴포넌트에서는 state라는 걸 사용해
![](https://velog.velcdn.com/images/ahk1106/post/340993ff-1e92-41e4-acca-5ba22df95f51/image.png)

>const[ count, setCount ] = useState(0)
> 사용법  -> console.log(count)
> 바꾸는 법-> setCount(1)

*State만 이해하면 document.getElementById().innerText 같은 복잡한 구조는 안 써도 된다. 훨씬 편하기 때문에!

* React의 State 방식
react에서는 자바스크립트 변수랑 html이 연결이 되어 있다. 그래서 변수값만 바꾸면 자동으로 html도 같이 바뀐다. 

```
const [ count, setcount ] = useState(0)
function zzz(){
	setCount(count + 1)
}
return ( 
 <div>
    <div>{count}</div>
    <button onClick={zzz}>카운트 증가!!</button>
 </div>
)
```

함수랑 함수형 컴포넌트랑은 다르다.
->html이 들어가 있으면 컴포넌트 없으면 함수

{} 안에는 자바스크립트를 넣을 수 있다.

#### 📌![](https://velog.velcdn.com/images/ahk1106/post/940016c4-80f5-44d8-84df-76567152279b/image.png)
