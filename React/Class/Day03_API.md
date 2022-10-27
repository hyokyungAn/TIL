* 개발자로서의 통신: 프로그램을 설치해서 사용한다.

<img width="1025" alt="스크린샷 2022-10-20 오전 3 17 12" src="https://user-images.githubusercontent.com/104885245/196772377-b847d4ae-cd82-4ddc-858f-2f8ad4e20047.png">

-HTTP: 통신

-API: 함수

-Graphql/Rest API: 통신방식

<img width="1025" alt="스크린샷 2022-10-20 오전 3 19 19" src="https://user-images.githubusercontent.com/104885245/196772740-eadf8b98-db1a-4ded-bec2-acb9c32d5073.png">

### 두 컴퓨터간 데이터 전송

<img width="840" alt="스크린샷 2022-10-20 오전 4 03 44" src="https://user-images.githubusercontent.com/104885245/196781266-7ed454d3-7de7-4e28-999b-46c2867bd434.png">

* 파일을 보내거나 메일을 전송하는 길을 만들고 싶다 ➡️ 각각의 관련 프로그램 설치(FTP, SMTP, HTTP) 

<img width="1042" alt="스크린샷 2022-10-20 오전 4 07 23" src="https://user-images.githubusercontent.com/104885245/196782075-38015e0b-507e-4e66-b1cb-def856d1a511.png">

+두 컴퓨터가 인터넷이 연결되어 있어야 함 ➡️ 두 컴퓨터가 데이터를 주고 받음.
* 데이터를 state에 예쁘게 포장해서 백엔드에 전송 ➡️ 그때 필요한 게 HTTP통신

### 관련 프로그램 설치하고 사용하는 방법

⬇️ HTTP 사용 규칙
<img width="1038" alt="스크린샷 2022-10-20 오전 4 12 43" src="https://user-images.githubusercontent.com/104885245/196783114-343817d4-040e-4b37-abd5-31e5b4186544.png">

* 요청을 하면 반드시 응답을 주게 되어 있음.

<img width="1074" alt="스크린샷 2022-10-20 오전 4 17 08" src="https://user-images.githubusercontent.com/104885245/196783698-230d350a-f5b5-40c1-b0d8-3bd34f292d9b.png">

* state들을  텍스트 형태 즉, 하나의 객체로 만들어서 백엔드에 요청(이 게시물 등록해줘~) → 백엔드에서 데이터를 받아서 DB(엑셀)컴퓨터에 게시물 저장 → 응답(완료됐어~)
* 총 3대의 컴퓨터(우리 컴퓨터, 백엔드 컴퓨터(서버 컴퓨터), 데이터베이스(DB)컴퓨터(엑셀이 깔려있는 컴퓨터)), 규모가 작을 경우 노트북으로도 가능

<img width="963" alt="스크린샷 2022-10-27 오후 10 19 33" src="https://user-images.githubusercontent.com/104885245/198295532-be00e4d6-b501-417d-beab-2d70b9ddc03d.png">

* 응답도 마찬가지로 객체형태로 데이터를 줄 수 있음
* 응답코드에는 상태코드(숫자)가 같이 옴 ➡️ 같은 의미를 가진 여러가지 경우의 수를 컴퓨터는 다 다르게 인식하기 때문에 상태 코드로 통일
   * 200: 성공
   * 400: 잘못된 요청
   * 403: 금지됨, 서버 요청 거부
   * 404: 찾을 수 없음
   * 500: 내부 서버 에러 

* 상태코드 참고:  https://ko.wikipedia.org/wiki/HTTP_%EC%83%81%ED%83%9C_%EC%BD%94%EB%93%9C


### API : 각각의 요청을 처리해주는 담당자, 쉽게 말해 해당 요청을 처리해주는 함수 

<img width="928" alt="스크린샷 2022-10-27 오전 1 20 02" src="https://user-images.githubusercontent.com/104885245/198080543-e26a64d0-957d-4b31-ae19-10845794aa4d.png">

* 3개의 담당자 즉, 3개의 함수
* 각각 요청과 응답으로 이루어져 있음.

### 담당자의 종류

<img width="980" alt="스크린샷 2022-10-27 오전 1 27 16" src="https://user-images.githubusercontent.com/104885245/198081972-d7eae75f-5790-42e6-b90a-ad97c5a7554e.png">

<img width="987" alt="스크린샷 2022-10-27 오전 1 41 26" src="https://user-images.githubusercontent.com/104885245/198085501-71e47657-4279-4a64-8e06-c2666fe01a56.png">

- `REST-API`(주소형태): axios 설치필요
    응답 결과로 back-end 개발자가 만든 함수에서 보내주는 모든 데이터를 다 받아와야되는 구조 ➡️ 백엔드에서 데이터를 프론트엔드로 많이 주게 되면 네트워크 비용을 많이 내야함(비효율적)

- `GRAPHQL-API`(함수형태) : apollo client 설치필요, REST-API보다 효율적, 페이스북에서 발생하는 수많은 데이터를 처리하기 위해 페이스북 개발팀에서 만들었으며,`facebook, airbnb, github` 등 유명한 사이트에서 사용중인 통신 방법

    필요한 정보만 받아오는 구조 ➡️ 네트워크 비용이 획기적으로 줌(서비스가 작을 땐 이점을 크게 느끼지 못하지만 커지면 효율적)

* 이러한 이유로, 각 API에 전송을 요청하는 담당자도 다름.
    * rest-API 에 요청하는 요청담당자는 `axios`
    * graphql-API 에 요청하는 요청담당자는 `apollo-client`

    ➡️ 요청담당자는 Front-end 에서 설치하는 라이브러리
    
⭐️ 설치해야 하는 도구와 이름이 다르지만 둘다 http 통신을 기반으로 하는 같은 방식으로 요청과 응답이 있고 응답에는 상태코드도 같이 첨부가 되어 있음.

### JSON
   
<img width="987" alt="스크린샷 2022-10-27 오전 1 46 13" src="https://user-images.githubusercontent.com/104885245/198086272-6f56cc66-1270-4926-84c6-23d069b66895.png">

* JSON(자바스크립트 객체 표기법): http 통신으로 데이터를 주고 받을 때 그때의 데이터 형태(자바스크립트 객체처럼 생겨서)

⭐️ 요청과 응답을 하면 JSON 형태로 데이터를 주고 받는다!!!

<img width="987" alt="스크린샷 2022-10-27 오전 1 57 23" src="https://user-images.githubusercontent.com/104885245/198088877-b4352316-0297-44d5-8c40-ef31fc52f398.png">

* 데이터를 주고 받을 때 헤더라는 부분이 포함되어 있음.
* 헤더의 역할: 응답, 요청에 대한 요약정보를 보여줌

➡️ 어떤 데이터가 보내질 것인지, 받을 건지, 누가 보내는지 이러한 요약 정보들이 헤더부분에 붙게 됨.

<img width="963" alt="스크린샷 2022-10-27 오전 2 00 44" src="https://user-images.githubusercontent.com/104885245/198089132-02889b2e-6dd2-4929-87b3-098b7398a7d9.png">

* 요청도 마찬가지!

### CRUD(크러드)

<img width="887" alt="스크린샷 2022-10-27 오전 2 04 53" src="https://user-images.githubusercontent.com/104885245/198090737-2e80e859-83f3-4410-806c-eaabb7a2b32e.png">

* **CRUD(create read update delete)**: 어떤 기능 혹은 api를 하나 만들 때 최소한의 CRUD가 구현되어야 함. ⭐️ 최소한의 5개의 API가 필요 (4 + 1) 
  * 게시글 목록에서 게시글 클릭해서 상세페이지로 들어가는 것 - 게시글 데이터를 백엔드로부터 읽어와서 화면에 보여준다(read)
  * 목록도 읽어와야 함 - 백엔드에서 목록 api 요청 (read)
      ➡️ read가 두개이기 때문에 + 1 해줘야 함 

![](https://velog.velcdn.com/images/ahk1106/post/8651a602-2d2b-4794-ac84-a28c5ca4dbf1/image.png)

* 데이터 베이스에 있는 엑셀을  변경(삭제, 추가) 즉,  수정이 들어가는 역할을 하는 매서드: POST(등록), PUT(수정), DELETE(삭제) - 엑셀 조작하는 기능
* 변경을 일으키는 애들을 graphql에서는 mutation이라고 부름(간소화)
* 조회는 변경 ❌ 

<img width="1004" alt="스크린샷 2022-10-27 오전 2 20 32" src="https://user-images.githubusercontent.com/104885245/198094016-103b20b2-9609-4a01-9a6c-3b6aeff3c8b3.png">

* rest-API를 알아야 하는 이유
1. graphql은 큰 서비스에 효율적, 그게 아닌 서비스들은 rest-API를 사용
2. 오픈 API(=public-API)등에서 rest-API를 주로 제공

<img width="1004" alt="스크린샷 2022-10-27 오전 2 28 26" src="https://user-images.githubusercontent.com/104885245/198095350-2d630d12-efcf-4c42-9672-29b62361334e.png">

* 둘 다 함수이지만 형태가 다름.
* '/board/1' 이름은 모두 같은데 메서드를 통해 구분해 효율적으로 사용 ➡️ rest-API이긴 한데 restful하다라고 표현
    이름은 변경할 수 있지만 많아지면 복잡하니까 똑같은 거 하나만 만들고 메서드를 다르게 해서 다른 함수를 실행시키자
* rest-API는 restful할 수도 있고 안 할 수도 있음. 백엔드에서 어떻게 만들었느냐에 따라 다름

### 설명서& 연습도구

<img width="1027" alt="스크린샷 2022-10-27 오전 2 42 29" src="https://user-images.githubusercontent.com/104885245/198098179-3d7ed473-00aa-4b4e-be6e-f099f9ea391d.png">

* `API 사용 설명서`: 홈페이지를 만들기 전, Back-end 개발자가 만들어 놓은 API 가 몇 개 있고, 어떻게 구성되어있는지 확인하기 위해 필요
* Back-end 개발자는 자신이 만든 API를 직접 문서 형태로 작성하거나, swagger 라는 프로그램을 설치해서 만듦.

#### REST-API

<img width="710" alt="스크린샷 2022-10-27 오후 5 41 24" src="https://user-images.githubusercontent.com/104885245/198236878-5ee80e23-8fc9-4dea-aaf8-55cd0e7c9f00.png">

<img width="878" alt="스크린샷 2022-10-27 오후 5 46 02" src="https://user-images.githubusercontent.com/104885245/198241228-44787151-6815-4c07-8e20-d35fce356d71.png">

⬇️ vscode에서 사용 방법
<img width="892" alt="스크린샷 2022-10-27 오후 6 29 26" src="https://user-images.githubusercontent.com/104885245/198247980-a486e8b6-7ce0-4c7a-af1b-f8cc22c5dfd2.png">

<img width="978" alt="스크린샷 2022-10-27 오후 5 46 51" src="https://user-images.githubusercontent.com/104885245/198241235-14a7b1e5-472f-4ae7-b74d-96bc41fe5750.png">

* 앞에 'http://주소' 가 생략된 것

<img width="731" alt="스크린샷 2022-10-27 오후 5 47 15" src="https://user-images.githubusercontent.com/104885245/198241237-f357e10a-d01e-40c7-abbd-b4db93267834.png">

<img width="1129" alt="스크린샷 2022-10-27 오후 6 18 14" src="https://user-images.githubusercontent.com/104885245/198245429-a94b43e1-5648-415e-bfd3-ca978ce73b82.png">

* 1번 게시물 가져와줘 요청 → 백엔드에서 DB컴퓨터로 들어가 엑셀에서 데이터를 찾아서 돌려줌 → 화면에 뿌리기
* 1000ms → 1초 // 83ms → 0.083s초가 걸림.
* 성공적으로 받아옴 ➡️ 상태코드 200
* 객체 형태로 받아오고 있음. ➡️ 객체 표기법(JSON) 
* JSON에는 배열도 포함됨.

#### GRAPHQL-API

<img width="811" alt="스크린샷 2022-10-27 오후 10 30 36" src="https://user-images.githubusercontent.com/104885245/198298128-121c7a89-5023-4638-9199-6c5d8e5f6945.png">

* String: "" 따옴표 붙여서 표현해야함.
* Int = integer의 약자로 정수, 숫자입력

<img width="1120" alt="스크린샷 2022-10-27 오후 6 42 42" src="https://user-images.githubusercontent.com/104885245/198251065-7187f47a-ddda-44fe-b85b-d10ac2d684f7.png">

* graphql은 받고 싶은 걸 골라 받을 수 있기 때문에 중괄호 안에 받고 싶은 데이터를 반드시 1개 이상 적어줘야 함.
* 다 받아와도 되지만 그렇게 되면 rest-API가 되는 것 
* Return 타입 ➡️ 백엔드 개발자가 만드는 타입

⬇️ 등록하기
<img width="1127" alt="스크린샷 2022-10-27 오후 9 37 54" src="https://user-images.githubusercontent.com/104885245/198288734-284c0c57-f0af-4916-bc5e-c31dc3529b88.png">

<img width="1127" alt="스크린샷 2022-10-27 오후 9 38 21" src="https://user-images.githubusercontent.com/104885245/198290919-8686fe34-5fc4-48e4-a974-def0e0a57a03.png">

* `CreateProductInput!`은 **객체** (원래 존재하는 게 아닌 백엔드 개발자가 만든 타입) ➡️ {}를 입력해줘야함.
* Return도 객체이기 때문에 반드시 {}를 써줘야함 → 그 안에 받고 싶은 데이터 작성해주기

⬇️ 목록 조회하기
<img width="1127" alt="스크린샷 2022-10-27 오후 9 15 02" src="https://user-images.githubusercontent.com/104885245/198281631-a21a9192-33f9-4476-9376-f3d51ca73d10.png">

* 한 번에 모든 게시물을 보여줄 수 없기 때문에 vscode에서 const result해서 변수에 저장해놓고 result에 있는 것을 for문(반복문)을 통해서 배열에 있는 객체들을 반복해서 화면에 뿌려주도록 해야함.
* 백엔드에서 page당 몇 개씩 끊어서 보여줄 지 설정해놓음.

⬇️ 해당 페이지 조회하기
<img width="1127" alt="스크린샷 2022-10-27 오후 9 19 52" src="https://user-images.githubusercontent.com/104885245/198282617-924a78d9-64c9-4277-be58-419dc880b059.png">

* 객체에 담겨서 받아와짐

⬇️ 수정하기
<img width="1120" alt="스크린샷 2022-10-27 오후 7 05 04" src="https://user-images.githubusercontent.com/104885245/198290296-8c7ff3c5-3c0c-458d-9491-e63f85231cd7.png">

* 수정조건(ID)에 해당하는 제품의 input안에 있는 내용들(수정대상) 수정해줘.
* 업데이트가 잘 됐는지 확인해보려면 fetchProduct로 가능

<img width="1123" alt="스크린샷 2022-10-27 오후 9 03 34" src="https://user-images.githubusercontent.com/104885245/198279415-d4a0dcc1-c454-405b-8639-f2ed45e190e1.png">

* !가 붙어 있는 것은 프론트와 백에서 데이터를 왔다갔다 할 때 필수적으로 있어야 하는 데이터, 안 보내줄 경우 에러 발생
* !가 없는 데이터는 빈값으로 보내줘도 상관없고 null로 받음. 

#### 📌![](https://velog.velcdn.com/images/ahk1106/post/740d35f7-9b9e-49e9-8d30-6dc4b8964d31/image.png)

봐도 봐도 어렵다 😢 살려조~ 
