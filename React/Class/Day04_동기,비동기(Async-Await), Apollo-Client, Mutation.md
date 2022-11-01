<img width="934" alt="스크린샷 2022-10-28 오전 1 15 50" src="https://user-images.githubusercontent.com/104885245/198343979-af9e4a13-4de5-48ba-9956-e088b0bf5116.png">


### 동기 vs 비동기

데이터를 요청하고 응답하기까지 시간을 기다릴 것이냐 안 기다릴 것이냐

<img width="913" alt="스크린샷 2022-10-28 오전 1 24 29" src="https://user-images.githubusercontent.com/104885245/198345884-39e54a81-ae99-43fa-b708-cffb1f5946e3.png">

⬇️ 원인

<img width="858" alt="스크린샷 2022-10-28 오전 1 19 57" src="https://user-images.githubusercontent.com/104885245/198344926-38cb52a6-2efe-46bb-977f-76d1c1996806.png">

* 등록이 완료되기 전에 불러오기 하면 안 불러와짐. 
* 등록하기 누르고 상세보기 화면을 바로 눌러버려서 빈칸이 뜬것

⬇️ 해결방법

<img width="858" alt="스크린샷 2022-10-28 오전 1 20 23" src="https://user-images.githubusercontent.com/104885245/198345044-7e973a7e-0d2c-4eb8-bbb0-ed9e619d63b7.png">

* 등록이 될 때까지 기다렸다가 상세보기 요청을 해야 됨
* 등록이 끝나면 불러오기를 해야하는 순서가 있는 경우에는 동기 방식을 사용

<img width="913" alt="스크린샷 2022-10-28 오전 1 25 31" src="https://user-images.githubusercontent.com/104885245/198347319-bcf223b6-b520-432c-bf88-16b3e6fb0972.png">

<img width="910" alt="스크린샷 2022-10-28 오전 1 30 43" src="https://user-images.githubusercontent.com/104885245/199354472-76e77ed3-6ce0-4a69-a46a-d83b74eb4132.png">

* 동시에 여러 일을 할 때, 뭐가 먼저 끝나든 상관이 없을 때(순서 상관x) 먼저 응답 받은 거 보여주면 됨 아무거나
  * 예) 게임 다운 받으면서 카톡하기

<img width="913" alt="스크린샷 2022-11-02 오전 3 50 29" src="https://user-images.githubusercontent.com/104885245/199314363-b45f0187-172d-4f3c-8c68-096a094497d9.png">

### VSCODE에서 비동기

<img width="961" alt="스크린샷 2022-11-02 오전 3 57 22" src="https://user-images.githubusercontent.com/104885245/199316028-4a249298-682c-490e-b2fe-cccf8893c394.png">

* 자바스크립트는 디폴트가 동기적 방식으로 작동. 쉽게 말해 끝날때까지 기다리는 것
* 라이브러리(외부에 요청하게끔 도와주는 axios같은 도구들)를 사용하게 되면 특정한 명령을 주지 않더라도 기본적으로 비동기식으로 작동. 기다리지 않는 것
* Promise: 언제 줄지는 모르지만 주긴 줄게라는 약속

→ http요청이 날라가게 되고 

→ 백엔드에 가서 데이터를 꺼내올 때까지 기다리지 않고 바로 아랫줄로 내려가버림

→ 기다려줘야 받은 내용을 data안에 저장해줄 수 있는데 비어있는 상황 

→ 언젠지는 모르겠지만 주긴 줄게의 promise만 들어가있는 것 

➡️ 기본적으로 비동기적으로 작동하기 때문에!

→ DB라는 엑셀에서 꺼내올 때까지 아랫줄로 내려가지 않고 기다려줘야 함

➡️ async(에이싱크, 어싱크)/await : 비동기작업을 동기로 바꿔주는 명령어, 기다리게 하는 명령어
   * async는 await가 실행되는 함수 앞에다가 적어준다
 
<img width="873" alt="스크린샷 2022-11-02 오전 4 18 09" src="https://user-images.githubusercontent.com/104885245/199319701-3ffb056f-54b5-4bb3-b56c-6a3efa02ac3b.png">

### 실습

#### rest

<img width="908" alt="스크린샷 2022-11-02 오전 4 58 46" src="https://user-images.githubusercontent.com/104885245/199327079-4310b51d-0f93-4b70-8b94-e5e5701a2049.png">

→ 버튼을 눌렀을 때 실행될 함수를 선언해주고 바인딩(연결)시켜줌

→ on으로 시작하는 속성에 들어갔으니까 event가 들어옴, 필요없으면 쓰지 않아도 됨 ➡️ 이벤트 핸들러 함수

→ axios 설치 후 import 해서 불러오기 

→ 화면에 보여주게 하기 위한 state 선언 ➡️ react에서 제공되는 기능으로 useState를 import 해줘야함

→ api 요청 → 해당 게시물을 백엔드에서 DB로 불러옴 → 불러올 때까지 기다렸다가 그 값을 객체로 받아와서 result에 저장

→ result에서 title 부분을 뽑아와서 State에 저장

→ "" 빈값이었던 내용이 title 로 바뀌게 됨 

<img width="818" alt="스크린샷 2022-11-02 오전 4 33 07" src="https://user-images.githubusercontent.com/104885245/199323335-c3363b52-2e19-4451-b7a2-e01067085170.png">

→ console 찍어보고 데이터 형태 파악 (확인용, 굳이 작성할 필요는 없음)

<img width="473" alt="스크린샷 2022-11-02 오전 4 24 02" src="https://user-images.githubusercontent.com/104885245/199320789-6663c783-774a-4935-bb6b-05e937324ada.png"> 

* react에서 onClick 함수이름은 handleClick, onClick으로 많이 사용 ➡️ 유지보수를 쉽게 하기 위해(고치기 쉽게) 다른 사람들이 많이 사용하는 코드(패턴)를 사용하는 것이 좋음

#### graphql

* 설치와 셋팅(_app.js)까지 필요

<img width="928" alt="스크린샷 2022-11-02 오전 5 16 50" src="https://user-images.githubusercontent.com/104885245/199332652-24ae5092-f6c0-44d3-822b-6b3c337e2029.png">

<img width="928" alt="스크린샷 2022-11-02 오전 5 19 35" src="https://user-images.githubusercontent.com/104885245/199333555-ff5b7245-fc04-40b5-be1e-d1dadfd0d93e.png">

* 실행함수를 요청하게 되면 어떤 api를 실행할 것인지 useMutation()안에 작성
* 실행함수() 명령을 실행하게 되면 api가 요청이 들어감

<img width="561" alt="스크린샷 2022-11-02 오전 5 26 52" src="https://user-images.githubusercontent.com/104885245/199334856-1224a0cc-1a32-49ba-a388-d683b2243f01.png">

* 이렇게 넣으면 복잡해지기 때문에 변수를 하나 만들어놓고 변수만 입력

<img width="581" alt="스크린샷 2022-11-02 오전 5 37 07" src="https://user-images.githubusercontent.com/104885245/199336185-0b344bc7-c303-45b2-9f1a-96808a59c80f.png">

* CREATE_BOARD라는 변수에 mutation내용을 담기 위해 '@apollo-client'를 import 해줘야함
* 여러 도구들이 있지만 많이 사용하는 apollo-client를 사용
* 변수에 담기 위한 도구 = gql(graphql약자)

<img width="581" alt="스크린샷 2022-11-02 오전 5 38 47" src="https://user-images.githubusercontent.com/104885245/199336460-5dc564e7-4f96-479b-b821-4457f71122f4.png">

* rest-api에서 axios.get()과 graphql-api에서 callGraphql()이 동일한 것

<img width="516" alt="스크린샷 2022-11-02 오전 5 46 08" src="https://user-images.githubusercontent.com/104885245/199337614-c8086cc9-648f-47e8-b4a4-acbd4936de25.png">

⭐️ _app.js에 셋팅이 필요

<img width="598" alt="스크린샷 2022-11-02 오전 6 00 14" src="https://user-images.githubusercontent.com/104885245/199339971-8d54f827-4280-4af0-87cc-06e2bd293108.png">

* rest는 백엔드 주소를 알지만 graphql은 모르기 때문에 주소를 알려주는 셋팅을 해줘야 함
* cache: 임시저장 
* ApolloProvider로 페이지 컴포넌트를 감싸주면 모든 페이지에서 useMutation을 사용할 수 있게 변경됨
* apollo-client 홈페이지에서 Get started 참조해서 사용

### 에러 디버깅 방법

* 개발자 도구 
   * Elements - html, css
   * Console - javascript 오류
   * Network - 통신관련 에러(백엔드 요청 확인, 인터넷이 끊겼는지 확인) 
  	 * graphql의 fetch 부분 확인

<img width="801" alt="스크린샷 2022-11-02 오전 6 37 24" src="https://user-images.githubusercontent.com/104885245/199346696-0fe285ad-b193-424b-ba02-8070f2f29084.png">

왜 한 번에 전달하지 않고 두 번에 걸쳐서 전달하지? 

<img width="801" alt="스크린샷 2022-11-02 오전 6 43 50" src="https://user-images.githubusercontent.com/104885245/199347553-90534ab9-1b0b-4caa-b2ea-41a712bec4e0.png">

* Graphql의 장점은 우리가 원하는 것을 골라서 받는 것인데 또 다른 장점은 **여러 Api를 하나로 묶어서 요청할 수 있다는 점**이다(네트워크 비용 절감)
* 묶음 배송해야 되기 때문에 하나의 Api를 보낸다고 하더라도 2번씩 써줘야 한다.
* 그룹에 writer를 보내면 각 api에 해당하는 writer항목에 분배해줌, 그룹 이름은 변경 가능

🙋🏻‍♀️ setData로 message, id, number 모두 보여주려면? 

<img width="547" alt="스크린샷 2022-11-02 오전 7 21 21" src="https://user-images.githubusercontent.com/104885245/199353070-069f36d6-1a0c-4e3a-a7fb-d47aee3a33d4.png">

<img width="547" alt="스크린샷 2022-11-02 오전 7 20 55" src="https://user-images.githubusercontent.com/104885245/199353083-85060da0-edfc-46da-91a6-0d439032610a.png">

* "" 문자열이 아닌 {} 객체를 써주고, setData에 객체 자체를 넣어줌

#### 📌![](https://velog.velcdn.com/images/ahk1106/post/6d2ee4b1-9a1e-4976-a9fb-2c8ee6d62801/image.png)
