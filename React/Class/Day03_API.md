응답코드에는 상태코드(숫자)가 같이 온다

*API : 요청을 처리해주는 담당자,쉽게 말해 해당 요청을 처리해주는 함수 

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
