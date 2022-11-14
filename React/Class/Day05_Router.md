<img width="917" alt="스크린샷 2022-11-15 오전 1 54 29" src="https://user-images.githubusercontent.com/104885245/201719033-5c2e3015-1baa-4daf-a098-429ca3d19e76.png">

### 라우팅 ➡️ 페이지 이동

<img width="917" alt="스크린샷 2022-11-15 오전 1 57 53" src="https://user-images.githubusercontent.com/104885245/201720596-018a5a21-3424-45d5-940b-ae6f04a68db8.png">

* **`라우터(router)` 객체**: 페이지 이동과 관련된 기능을 가지고 있는 객체

➡️ 이 객체를 사용해서 A 페이지에서 B 페이지로 이동할 때, "B 페이지로 라우팅한다"고 함.

#### 자주 사용하는 라우터(router) 객체 기능

```jsx
import Router from 'next/router'

export default function Routing() {
    const handleClickPathname = () => {
        const pathname = Router.pathname
        alert(pathname)
    }

    const handleClickAsPath = () => {
        const asPath = Router.asPath
        alert(asPath)
    }

    const handleClickBack = () => {
        Router.back()
    }

    const handleClickPush = () => {
        Router.push('/')
    }

    const handleClickReload = () => {
        Router.reload()
    }

    const handleClickReplace = () => {
        Router.replace('/')
    }


    return (
      <>
        <button onClick={handleClickPathname}>현재 위치 주소: Router.pathname</button><br/>
        <button onClick={handleClickAsPath}>현재 위치 주소: Router.asPath</button><br/>
        <button onClick={handleClickBack}>뒤로가기 버튼: Router.back()</button><br/>
        <button onClick={handleClickPush}>현재 페이지에서, 다른 페이지로 이동: Router.push()</button><br/>
        <button onClick={handleClickReload}>새로고침: Router.reload()</button><br/>
        <button onClick={handleClickReplace}>현재 페이지 삭제 후, 다른 페이지로 이동: Router.replace()</button><br/>
      </>
    )
  }
```

### 페이지 조회

<img width="1036" alt="스크린샷 2022-11-15 오전 2 21 27" src="https://user-images.githubusercontent.com/104885245/201725140-efbc5fdd-6c38-4000-b919-59414ad5a91e.png">

* useMutation과 useQuery의 차이점: useMutation은 게시글 등록하기를 클릭했을 때 함수가 실행이 되지만 useQuery(조회하기)는 바로 요청이 들어감.

<img width="1036" alt="스크린샷 2022-11-15 오전 2 36 57" src="https://user-images.githubusercontent.com/104885245/201728087-bad64757-af64-4788-8c5d-272d1cf76859.png">

* data를 받아오기까지 undefined상태이기 때문에 error 발생

<img width="1036" alt="스크린샷 2022-11-15 오전 2 38 16" src="https://user-images.githubusercontent.com/104885245/201728376-01a4cb2c-6db4-418c-bed7-6f304f973b85.png"> 

* data가 언제 받아와질지 모른 채 흰색 배경화면만 보여줘야하는 상황이 발생, 조금이라도 빠르게 보여주기 위해서 보여줄 수 있는 것들 먼저 보여주고 알맹이들은 늦게 보여주면 됨

<img width="1041" alt="스크린샷 2022-11-15 오전 2 47 05" src="https://user-images.githubusercontent.com/104885245/201730356-a76eacb4-15cd-432b-b820-43b9160cf3e0.png">

* {data && data.fetchBoard.number} ➡️ 조건부렌더링: 데이터가 있을 때 뒤에거 보여줘 없으면 앞에거 보여줘!
* 데이터 받아올 때까지 기다리면 너무 느리고 답답함을 줄 수 있기 때문에 데이터 빼고 나머지를 먼저 보여줌

<img width="1041" alt="스크린샷 2022-11-15 오전 2 52 37" src="https://user-images.githubusercontent.com/104885245/201731271-3bdaa67e-c94c-40a4-b9a1-255347a33610.png">

* {data && data.fetchBoard.number} = {data?.fetchBoard.number} ➡️ 옵셔널체이닝: 기존의 && 연산자를 쓰면서 길어졌던 코드를 더욱 간결하게 사용하는 연산자 
* ?연산자 앞 객체의 참조가 **undefined || null**이라면 **undefined**를 리턴해줍니다. 

위에 있는 삼항연산자, && 연산자와 똑같은 기능

### 라우팅 종류

<img width="935" alt="스크린샷 2022-11-15 오전 2 56 51" src="https://user-images.githubusercontent.com/104885245/201732145-b46f32ba-ba88-4924-a1f3-0c67d9a53f4d.png">

* 정적라우팅: /login 페이지는 누가 언제 접속해도 항상 로그인 페이지가 나옴 ➡️ 이러한 페이지로 이동하는 것을 **"정적 라우팅한다"** 고 함

* 동적라우팅: 게시판 상세보기와 같은 경우, 글 번호에 따라서 주소가 변경됨. 이러한 경우에는 게시글이 100개, 1000개가 넘어가게 되면 각각의 글 번호에 따라 페이지를 100개, 1000개씩 만들어 정적라우팅을 해주기는 어렵기 때문에 이러한 라우팅을 효과적으로 처리하기 위해서 **동적 라우팅**을 사용

* /boards/aaa가 아님!!
* 페이지를 의미하는 게 아닌 **변수**를 의미 ➡️ 변수에 담김

```
next.js에서는 동적 라우팅을 제공해줌

보여주고자 하는 폴더 이름의 하위 폴더로 [아무이름의]폴더를 만들어 준 후 이 안에 index.js 파일을 만들어주면 동적 라우팅을 사용할 수 있음 

대괄호로 감싸준 폴더를 만들어주면 이동하고자 하는 페이지 번호, 혹은 게시글 번호가 대괄호 안에 쓰여진 변수명에 담겨져 그 변수 안에 있는 데이터를 꺼내 조회할 수 있음

대괄호 안에 쓰여지는 폴더 이름은 단순히 변수명이기 때문에 어떻게 작성해도 상관없음. 이러한 과정을 router 객체가 도와주는 것!!

router.query = { aaa: 1} 이런 형식으로 들어가게 되면서 자동으로 게시글 번호를 꺼내올 수 있음
```

<img width="987" alt="스크린샷 2022-11-15 오전 3 03 44" src="https://user-images.githubusercontent.com/104885245/201733492-1ad8b37d-47a0-400a-b106-65823cedb77a.png">

* 하나의 페이지에서 여러 주소로 동적으로 바뀌도록 함 ➡️ 페이지를 하나만 만들어놓고 다이나믹하게 사용

#### 템플릿 리터럴

<img width="987" alt="스크린샷 2022-11-15 오전 3 39 44" src="https://user-images.githubusercontent.com/104885245/201740881-9dc981e0-6bd8-4ba9-9e30-e8a4a8c87ac7.png">
