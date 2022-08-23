### 🌱 게시글 등록 시 상세 페이지가 보이도록 동적 라우팅(조건부렌더링, try~catch) 

![](https://velog.velcdn.com/images/ahk1106/post/e89829dd-52db-4f6a-abf5-d0240f1f387c/image.png)
* 1. 구조, 배치 파악 2. 데이터들을 어떻게 받아 오고 있는지

![](https://velog.velcdn.com/images/ahk1106/post/0f040450-a244-4760-9fce-9185c3bf50e4/image.png)

![](https://velog.velcdn.com/images/ahk1106/post/c768010e-b725-4918-a589-d51a02f0de04/image.png)

![](https://velog.velcdn.com/images/ahk1106/post/8a38a26f-e82d-4ed0-8532-64fdafc271a1/image.png)

* 등록을 하면 등록한 게시물에 대한 id를 받을 수 있었기 때문에 등록이 끝날때까지 기다려야 그 안에 id가 들어갔음
* 등록 → 백엔드 API → 데이터베이스(데이터를 집어넣어서 아이디 생성) → 아이디를 다시 돌려주면 → 돌려받은 아이디를 result에 담고 → 담은 아이디를 가지고 상세페이지로 이동
그렇기때문에 무조건 기다려줬어야함! ➡️ await (동기식)

![](https://velog.velcdn.com/images/ahk1106/post/d64bcc49-e431-413f-8f24-ea427b41ba33/image.png)

![](https://velog.velcdn.com/images/ahk1106/post/e37fa6ac-ff8d-4f61-b92f-ea60782b6ce8/image.png)

![](https://velog.velcdn.com/images/ahk1106/post/c8116532-19c5-44a6-932b-f1553c6c6dc1/image.png)
