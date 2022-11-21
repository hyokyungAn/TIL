<img width="901" alt="스크린샷 2022-11-18 오전 1 25 19" src="https://user-images.githubusercontent.com/104885245/202502300-b74bd108-7b60-4985-a656-8ee653ffc98b.png">

<img width="901" alt="스크린샷 2022-11-18 오전 1 26 01" src="https://user-images.githubusercontent.com/104885245/202502350-35ab17ac-3295-4f32-81a4-c28ba8440e92.png">

* !DOCTYPE으로 시작하는 html 문서의 가장 윗부분 코드는 우리가 브라우저에게 제공하려고 하는 현재의 html이 웹표준에 의거해 실행되도록 해주세요라고 명시하는 부분

<img width="925" alt="스크린샷 2022-11-22 오전 1 47 28" src="https://user-images.githubusercontent.com/104885245/203112447-b9a324b1-f43e-4544-8787-d1555cf1d9a2.png">

* <html> - 시작 / </html> - 종료 : html파일을 태그가 시작하는 곳부터 끝나는 부분까지 작성해서 브라우저에게 제공하겠습니다라고 약속하는 범위
* 브라우저에게 알려주는 이유: html문서는 웹브라우저에서 시작하기 때문에 
* 왜 범위가 필요한가?: 정해진 규칙에 따라서 코드를 작성해야 하고 브라우저가 이해할 수 있는 내용(명령)들로 문서를 작성해야 함! 

<img width="925" alt="스크린샷 2022-11-22 오전 1 57 42" src="https://user-images.githubusercontent.com/104885245/203114758-4b92cd06-2759-4024-a9bb-a0353ec2b95a.png">

<img width="925" alt="스크린샷 2022-11-22 오전 2 00 34" src="https://user-images.githubusercontent.com/104885245/203115200-7e92e0ed-d5f0-415e-be91-9dad69d59fb6.png">

* head와 body 각각 해석하고 사용하는 방식이 다름

<img width="925" alt="스크린샷 2022-11-22 오전 2 11 54" src="https://user-images.githubusercontent.com/104885245/203118063-3069627e-91cf-49a1-b3fe-b318fbb7f7d8.png">

* lang(language의 약어)은 지정할 문서의 언어(ISO 639-1)를 명시하는 HTML 속성 
* 외부의 파일을 가져와서 내부에 연결하는 행위: 정보 - head 태그에 작성

<img width="808" alt="스크린샷 2022-11-22 오전 2 16 44" src="https://user-images.githubusercontent.com/104885245/203119237-7aa54e8f-e47f-4079-84f0-a4c0bcc9b9be.png">

<img width="826" alt="스크린샷 2022-11-22 오전 2 18 35" src="https://user-images.githubusercontent.com/104885245/203119475-c5fac8ff-988b-44ed-8e90-d6d4988cac53.png">

* href라는 속성을 통해 가지고 온 특정한 파일이 html과 어떤 관계를 가지는지 rel이라는 속성에다가 명시를 해줘야 함
➡️ rel(Relationship 단어의 약어)은 가져올 외부 문서(대표적으로 CSS 파일)가 현재의 HTML과 어떤 관계인지를 명시하는 HTML 속성
➡️ href(Hyper Text Reference 단어의 약어)는 브라우저가 참조할 특정 경로를 지정하는 HTML 속성 

<img width="797" alt="스크린샷 2022-11-22 오전 2 25 32" src="https://user-images.githubusercontent.com/104885245/203120821-f4440254-dfcf-46e6-9146-acb9062f55a3.png">

<img width="807" alt="스크린샷 2022-11-22 오전 2 26 35" src="https://user-images.githubusercontent.com/104885245/203121030-24001527-9ced-4f7f-ace9-ace4d3f073ff.png">

* main.css 파일을 만들어서 link로 가지고 오는 것과 style 태그에다가 직접적으로 작성하는 방식 - 스타일의 선언 방식에 차이가 있다라고 얘기함

<img width="839" alt="스크린샷 2022-11-22 오전 2 31 10" src="https://user-images.githubusercontent.com/104885245/203122358-5c226eac-b4ee-4e63-8b5c-c15af787fac1.png">

* src(Source 단어의 약어)는 사용할 소스코드(파일)를 지정하는 HTML 속성
* src를 사용하면 외부에 있는 자바스크립트 파일을 가져오는 경우(link)/ 사용하지 않으면 내부에 직접적으로 작성하는 방식(style)
* link태그와 style태그를 동시에 가지고 있고 사용할 수 있음

<img width="1056" alt="스크린샷 2022-11-22 오전 2 36 23" src="https://user-images.githubusercontent.com/104885245/203123164-8ef4f872-17b7-438c-bd92-e4e92dc49178.png">

* meta태그는 link, style, script,title 각각의 태그로 나타낼 수 없는 나머지 모든 정보들을 표시할 때 사용하는 태그
* charset(Character Set 단어의 약어)은 문자 인코딩 방식을 지정하는 HTML 속성
 ➡️ 문자 인코딩: 문자나 기호들을 컴퓨터가 이용할 수 있는 신호로 만드는 것, 대표적으로 한글 사용에서는 EUC-KR 혹은 UTF-8 등이 사용되며, 웹에선 UTF-8의 사용을 권장
 
<img width="933" alt="스크린샷 2022-11-22 오전 2 39 03" src="https://user-images.githubusercontent.com/104885245/203123685-e6c60cb7-c201-46a1-952a-8d9fb2833b11.png">

<img width="969" alt="스크린샷 2022-11-22 오전 2 52 49" src="https://user-images.githubusercontent.com/104885245/203125937-d7b36ba7-f36f-48ac-a988-3ea2c6aa2893.png">

* 브라우저는 프로젝트 폴더에 들어가자마자 index.html 파일을 찾아서 실행하기 때문에 
  프로젝트의 최상위 경로(Root path)에 index.html 파일이 존재해야지만 브라우저가 파일을 자동으로 찾아서 브라우저에 출력할 수 있음
  ➡️ 그렇기 때문에 따로 폴더를 만들어서 html 파일들을 관리하면 안 됨!!! 
  
<img width="696" alt="스크린샷 2022-11-22 오전 3 07 19" src="https://user-images.githubusercontent.com/104885245/203128622-4de48551-90c8-4e61-975c-55e04bac55aa.png">

* alt(Alternate 단어의 약어)는 이미지가 출력되지 못하는 경우 대신 출력할 텍스트, 대체 텍스트
* 이미지를 출력할 때 작성해야하는 필수 속성
