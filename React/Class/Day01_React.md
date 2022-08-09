⭐️ 초반에 해야할 것
1. 영타 실력 늘리기
2. 단축키 사용
3. 코드 리딩 실력 키우기(기존에 있는 코드들을 읽는 능력이 중요)


#### GUI(Graphic User Interface)
:화면에서 마우스를 통해 컴퓨터를 조작하는 그래픽 기반의 유저 인터페이스

#### CLI(Command Line Interface)
:터미널에서 텍스트를 통해 폴더를 만들고 이동하는 등의 컴퓨터를 조작하는 명령어 기반의 인터페이스

#### 터미널
:컴퓨터와 사용자 간 소통을 위한 인터페이스

➤ 맥 유저) command + space를 누르고 ‘터미널’(terminal)이라고 입력하면 실행됨.

> ls(list): 내가 있는 폴더 목록을 보여줘
> 
> pwd(print working directory): 내가 있는 폴더 알려줘
>
> directory = 폴더
>
> mkdiv(make directory): 폴더 만들기
>
> cd(change directory): 만들 폴더 안으로 이동
>
> cd ..: 폴더 나가기

***React**: 자바스크립트를 쉽고 효율적으로 사용할 수 있도록 페이스북에서 만든 도구

➤ 하나로 두 개의 기능을 처리해 효율적

➤ next는 react의 업그레이드 버전으로 설치하면 react가 자동으로 포함

***보일러 플레이트**: React의 초기 셋팅이 완료된 폴더

> pages: 프론트엔드의 페이지 화면들을 모아놓은 폴더, 내가 작성할 페이지
>
> public: 사진, 아이콘 등
>
> styles: css파일
> 
> package.json: 핵심이 되는 파일로 설명서, 실행 방법이 적혀있는 페이지
> 
> README.md: 상세 설명서

-class폴더 안 이동 먼저(cd class)

-app.js: 설정 파일(모든 페이지가 실행되기 전 맨 처음 한 번 실행되는 설정 파일)

-pages: 첫 시작 페이지 의미 = /

***import(불러오기)와 export(내보내기)**
React에서 다른 폴더에 있는 파일을 불러 올 수 있다.
export가 있는 애들에 한해서 import가 가능하다.
우리가 만드는 소스코드는 주로 HTML, CSS, JAVASCRIPT이다.
하나의 소스코드에 이 모든 내용을 코딩하면 너무 복잡해져 HTML, CSS, JAVASCRIPT를 작성하는 소스코드 파일을 각 각 따로 만들고, 필요에 따라 서로 불러와서 사용하게 된다.

***JSX**: React에서 사용하는 **React 전용 HTML**
기존 HTML방식과 속성값의 대소문자 정도 차이 등을 제외하곤 거의 비슷하다.
웹브라우저는 HTML, CSS, JAVASCRIPT만 읽을 수 있어 최종적으로 소스코드가 실행될 때는 JSX가 HTML로 자동으로 변환되어 실행된다.
![](https://velog.velcdn.com/images/ahk1106/post/fb98fcb1-232e-44f7-8561-5871f21875d3/image.png)

***CSS(CSS-IN-JS) - emotion**은 CSS를 JS상수에 저장해서 사용하는 방법
이렇게 저장한 상수는 HTML 태그처럼 사용할 수 있다.
![](https://velog.velcdn.com/images/ahk1106/post/eb022cd8-2039-4aa9-adcc-d56b97c6721a/image.png)
1._태그에 의미를 부여할 수 있어서, 태그만 봐도 결과물이 예상_된다.
2. className을 입력하지 않아도 되기 때문에, _코드가 간결해지고 단축돼 읽기 쉬운 코드_가 된다.
3. _코드 재사용성_이 증가한다. -한 번 만들어놓고 여러 곳에 복사해서 사용하는 것

=>HTML+CSS를 합쳐서 나만의 태그(div)를 만들어 변수에 담아서(const Title) 사용.

*styled-components랑 emotion은 거의 동일하다.

* CSS 코드

> #### justfy-content
>flex-start - 왼쪽 정렬
>flex-end - 오른쪽 정렬
>center - 가운데 정렬
space-between -  사이에 동일한 간격
space-around - 주위에 동일한 간격
#### align-items  
flex-start - 꼭대기 정렬
flex-end - 바닥 정렬
center - 세로선 상 가운데 정렬
baseline - 시작 위치 정렬
stretch - 컨테이너에 맞도록 늘림              
#### flex-direction 
row - 텍스트의 방향과 동일 정렬
row-reverse - 텍스트의 반대 방향
column - 위에서 아래로 정렬
colunm-reverse - 아래에서 위로 정렬

📌![](https://velog.velcdn.com/images/ahk1106/post/4e31e408-704b-4d1a-a5f8-329eca69f9ec/image.png)

