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

### 컴포넌트 만드는 방법 2가지
-컴포넌트는 함수로밖에 못 만드는 것인가? No! ➡️ 함수형이 존재하기 이전에는 클래스형이 존재(클래스형 컴포넌트)

<img width="908" alt="스크린샷 2022-10-13 오전 2 20 31" src="https://user-images.githubusercontent.com/104885245/195407729-451e7613-2814-4d7e-af3c-28f5d9c55777.png">

-기존에는 클래스형을 쓰다가 최근에는 함수형으로 넘어가는 추세, 왜 함수형을 쓰는가? ➡️ 코드길이가 짧음 
* function이 하나의 컴포넌트이다 ➡️ 함수형 컴포넌트
* 함수형 컴포넌트 ➡️ 화살표 함수로 표현 가능(코드길이가 짧아진다)

### React-Hooks
-처음부터 쓰지 왜 이제서야 함수형을 쓰는 거야? ➡️ 이후에 use로 사용하는 기능이 생김. (리액트 업데이트)

컴포넌트가 언제 만들어져야하는지 언제 사라져야하는지 데이터를 저장하는 기능들이 가능해지도록 업데이트 됨. ➡️ 앞에 use가 붙은 기능들(hooks)

* 함수형 컴포넌트가 클래스형 컴포넌트보다 간단
* 하지만, 함수형 컴포넌트 그 자체만으로는 클래스형 컴포넌트의 모든 기능을 흉내낼 수 없어 React 에서 함수형 컴포넌트에서도 클래스형 컴포넌트와 동일한 기능을 사용 가능하도록 도구를 만듦.
* 이 도구를 **Hooks(훅)** 이라고 부름.

⭐️ **React-Hooks의 함수형 컴포넌트**: Hooks는 함수형을 클래스형과 동일한 기능을 사용 가능하도록 만들어 줌. 덕분에 함수도 컴포넌트 형태로 사용할 수 있게 됨.

* 대표적인 Hooks 에는 `useState`, `useEffect`가 있음.

* 클래스형과 함수형은 섞어 쓸 수 있다. 
* 클래스형을 함수형으로 변경 가능하다.

### State: 컴포넌트 전용 변수

* state: 컴포넌트에서 사용하는 변수
* setState: 컴포넌트에서 사용하는 변수를 바꿔주는 기능(함수) 
* useState: 컴포넌트에서 사용하는 변수를 만들어주는 기능
* useState라는 기능이 있어야 변수를 만들 수 있다.

-변수는 let, const로 만드는 거 아니었어? ➡️ 맞아 그런데 컴포넌트에서는 state라는 걸 사용해

![](https://velog.velcdn.com/images/ahk1106/post/340993ff-1e92-41e4-acca-5ba22df95f51/image.png)

<img width="977" alt="스크린샷 2022-10-13 오전 2 46 50" src="https://user-images.githubusercontent.com/104885245/195412585-fb4e0a2f-43a6-4592-926e-bdbf0527d5f7.png">

#### 변수값 변경하는 방법

<img width="977" alt="스크린샷 2022-10-13 오전 2 48 49" src="https://user-images.githubusercontent.com/104885245/195412950-56ff0784-f738-4820-823f-cb0f2747308a.png">

-기존 방식이 편한데 이걸 왜 사용할가? ➡️ State만 이해하면 document.getElementById().innerText 같은 복잡한 구조는 안 써도 된다. 훨씬 편하기 때문에!

<img width="977" alt="스크린샷 2022-10-13 오전 2 52 52" src="https://user-images.githubusercontent.com/104885245/195413692-f4d69f32-6b5a-491c-8d27-679edc6faf5f.png">

<img width="977" alt="스크린샷 2022-10-13 오전 2 56 38" src="https://user-images.githubusercontent.com/104885245/195414454-e909d905-1eb7-4394-b297-d173a1d9375a.png">

* react에서는 자바스크립트 변수랑 html이 연결이 되어 있음. 변수값을 바꾸면 자동으로 html도 같이 바뀜.
* let을 사용하게 되면 리액트 전용 변수가 아니기 때문에 html이 연결되어 있지 않음. 기존 방식을 사용해야 함.  

-함수랑 함수형 컴포넌트랑은 다를까? Yes! ➡️ html이 들어가 있으면 함수형컴포넌트, 없으면 기존에 배운 함수

<img width="977" alt="스크린샷 2022-10-13 오전 3 31 57" src="https://user-images.githubusercontent.com/104885245/195420909-9edf3a01-b0ad-4623-8e72-ecac72bbd74b.png">

* state를 사용하는 이유: 입력값을 예쁘게 포장해놓기 위해

-> 백엔드API(함수)에 포장한 내용을 보내줌 -> DB(엑셀)에 값을 저장.

<img width="895" alt="스크린샷 2022-10-13 오전 3 35 13" src="https://user-images.githubusercontent.com/104885245/195421521-dfb36757-3573-463a-99b9-077802eff739.png">

* onChange={} ➡️ 변경될 때마다 onChange함수 실행
* onChange, onClick 등 on으로 시작하는 애들은 html과 자바스크립트를 연결시켜 주는 특별한 속성!
* 입력하면 자동으로 event라는게 들어오게 된다.

<img width="520" alt="스크린샷 2022-10-13 오전 3 45 42" src="https://user-images.githubusercontent.com/104885245/195423479-476e6438-28d4-428f-90d4-b7712695a9ac.png">

* event.target 하면 태그가 가지고 와짐. 어디가 변경돼서 이 함수가 실행이 되었는지 ➡️ 태그전체를 의미
* event.target.value 하면 값을 가지고 옴

<img width="708" alt="스크린샷 2022-10-13 오전 3 52 51" src="https://user-images.githubusercontent.com/104885245/195424691-83e3b861-3342-4283-8f56-4a7eefd80a96.png">

* 함수를 연결시켜 놓음 ➡️ 바인딩했다 라고 표현(바인드 = 연결)
* let을 써도 작동하지만 직접적으로 바꾸는 것도 가능, 이런 문제를 막기 위해 실무에선 const 사용.
* 초기값을 비워두면 아무것도 안 뜨다가 에러시 메시지가 뜸

#### 📌![](https://velog.velcdn.com/images/ahk1106/post/940016c4-80f5-44d8-84df-76567152279b/image.png)
