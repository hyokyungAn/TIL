기존에 아는 것과 다른 새로운 게 나왔다면 이게 더 좋나? 라는 의심을 해볼 필요가 있다. 기존에 있던 문제점을 개선해서 나온 게 대부분!

<img width="857" alt="스크린샷 2022-10-11 오후 4 14 54" src="https://user-images.githubusercontent.com/104885245/195020906-042398fb-0963-4c56-8232-d7f55c262625.png">

<img width="1023" alt="스크린샷 2022-10-11 오후 4 57 24" src="https://user-images.githubusercontent.com/104885245/195032249-585128f5-9f82-4f6a-9b44-51d0880faefc.png">

대표적인 프론트엔드 도구로는 React, Angular, Vue가 있다. 이 가운데
### react를 배워야 하는 이유
1. 가장 많은 이용자 - 커뮤니티 활성화: 모르는 걸 물어볼 사람이 많다, 취업할 곳도 많다.  
3. 웹, 앱, 데스크탑앱 모두 만들 수 있다. - All In One

<img width="890" alt="스크린샷 2022-10-11 오후 5 15 08" src="https://user-images.githubusercontent.com/104885245/195036047-fba48190-6687-4211-bf98-8d4b387df754.png">

* 순수 자바스크립트와 어떤 차이가 있어 React, Angular, Vue로 넘어오게 됐는가? 그 이유는 component 이다!

### React의 핵심 Component 

* 컴포넌트란 **UI 또는 기능을 부품화해서 재사용**가능하게 하는 것
* component를 조립해서 하나의 페이지를 찍어낸다. 
* 부품만 잘 만들어놓으면 여러군데에서 원하는 대로 사용할 수 있음.
* 기본적으로는 원본이 통제하고 원본만 변경하면 모두 적용 가능. 원하는 부분들(글자 등)은 바꿔 쓸 수 있다.(UI의 재사용, 효율적)

➡️ 복사+붙여넣기와 다른 이유: 수정이 필요할 경우 모든 게시물 하나하나 수정.(비효율)

<img width="915" alt="스크린샷 2022-10-12 오후 11 45 30" src="https://user-images.githubusercontent.com/104885245/195374625-faccd025-d68f-45d7-888b-56ab37a22261.png">

* 컴포넌트 안에 컴포넌트가 들어가는 것도 가능함.
* 반복적으로 필요한 부분을 컴포넌트로 만들어서 import해서 사용
* 페이지 전체도 컴포넌트로 볼 수 있음 ➡️ 페이지 컴포넌트

<img width="915" alt="스크린샷 2022-10-12 오후 11 49 23" src="https://user-images.githubusercontent.com/104885245/195375469-29809c16-9adb-4a5b-b120-da5fd043a780.png">

#### 컴포넌트는 두가지 유형이 있다.

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

#### state: 컴포넌트 전용 변수
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
