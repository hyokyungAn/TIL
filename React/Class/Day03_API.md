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

+두 컴퓨터가 인터넷이 연결되어 있어야 함. ➡️ 두 컴퓨터가 데이터를 주고 받음.
* 데이터를 state에 예쁘게 포장해서 백엔드에 전송 ➡️ 그때 필요한 게 HTTP통신

### 관련 프로그램 설치하고 사용하는 방법

* HTTP 사용 규칙

<img width="1038" alt="스크린샷 2022-10-20 오전 4 12 43" src="https://user-images.githubusercontent.com/104885245/196783114-343817d4-040e-4b37-abd5-31e5b4186544.png">

* 요청을 하면 반드시 응답을 주게 되어 있음.

<img width="1074" alt="스크린샷 2022-10-20 오전 4 17 08" src="https://user-images.githubusercontent.com/104885245/196783698-230d350a-f5b5-40c1-b0d8-3bd34f292d9b.png">

* state들을 하나의 객체로 만들어서 백엔드에 요청 ➡️ 데이터를 받아서 DB(엑셀)컴퓨터에 저장 ➡️ 응답(완료)
* 총 3대의 컴퓨터

<img width="1042" alt="스크린샷 2022-10-20 오전 4 21 45" src="https://user-images.githubusercontent.com/104885245/196784589-92a39185-f77a-4175-aec6-e8b323f37b59.png">

* 응답코드에는 상태코드(숫자)가 같이 옴.
   * 400: 잘못된 요청
   * 403: 서버 요청 거부
   * 404: 찾을 수 없음
   * 500: 내부 서버 에러 

* 참고:  https://ko.wikipedia.org/wiki/HTTP_%EC%83%81%ED%83%9C_%EC%BD%94%EB%93%9C


### API : 요청을 처리해주는 담당자,쉽게 말해 해당 요청을 처리해주는 함수 

*담당자의 종류
-Rest-API : 주소처럼 생긴 이름(http:~~), 백엔드에서 데이터를 프론트엔드로 많이 주고 받게 되면 네트워크 비용을 많이 내야함.
→이름은 모두 같은데 메서드를 통해 구분해 효율적으로 사용하는 방식: restful
-Graphql-API : 함수처럼 생긴 이름( board(1), profile("철수")),
1번 게시글 작성자, 제목만 가져다줘! -네트워크 비용이 획기적으로 줌
➡️ 생긴 게 조금 다르지만 http 통신을 기반으로 하는 같은 방식
   
*요청과 응답을 하면 **JSON(자바스크립트 객체 표기법)** 형태로 데이터를 주고 받는다.

*헤더: 응답, 요청에 대한 요약정보를 보여줌, Application/json

***CRUD(create read update delete)**: 어떤 기능이 하나 추가된다라는 것은 최소한의 5개의 API 가 필요 (4개 + 1 -read가 2개)  
![](https://velog.velcdn.com/images/ahk1106/post/8651a602-2d2b-4794-ac84-a28c5ca4dbf1/image.png)

axios : 주는대로 다 받기
apollo-client: 골라서 받기(효율적)


#### 📌![](https://velog.velcdn.com/images/ahk1106/post/740d35f7-9b9e-49e9-8d30-6dc4b8964d31/image.png)
