<img width="934" alt="스크린샷 2022-10-27 오후 10 41 57" src="https://user-images.githubusercontent.com/104885245/198342613-7b2c3069-09d4-4534-850f-e1aace9cd2be.png">

<img width="934" alt="스크린샷 2022-10-28 오전 1 15 50" src="https://user-images.githubusercontent.com/104885245/198343979-af9e4a13-4de5-48ba-9956-e088b0bf5116.png">


### 동기 vs 비동기

데이터를 요청하고 응답하기까지 시간을 기다릴 것이냐 안 기다릴 것이냐

<img width="913" alt="스크린샷 2022-10-28 오전 1 24 29" src="https://user-images.githubusercontent.com/104885245/198345884-39e54a81-ae99-43fa-b708-cffb1f5946e3.png">

⬇️ 원인

<img width="858" alt="스크린샷 2022-10-28 오전 1 19 57" src="https://user-images.githubusercontent.com/104885245/198344926-38cb52a6-2efe-46bb-977f-76d1c1996806.png">

* 등록이 완료되기 전에 불러오기 하면 안 불러와짐. 
* 등록하기 누르고 상세보기 화면을 바로 눌러버려서 빈칸이 뜬것 ➡️ 비동기

⬇️ 해결방법

<img width="858" alt="스크린샷 2022-10-28 오전 1 20 23" src="https://user-images.githubusercontent.com/104885245/198345044-7e973a7e-0d2c-4eb8-bbb0-ed9e619d63b7.png">

* 등록이 될 때까지 기다렸다가 상세보기 요청을 해야 됨 ➡️ 동기(게시글 등록→등록완료→게시글 불러오기)
* 등록이 끝나면 불러오기를 해야하는 순서가 있는 경우에는 동기 방식을 사용

<img width="913" alt="스크린샷 2022-10-28 오전 1 25 31" src="https://user-images.githubusercontent.com/104885245/198347319-bcf223b6-b520-432c-bf88-16b3e6fb0972.png">

<img width="913" alt="스크린샷 2022-10-28 오전 1 30 43" src="https://user-images.githubusercontent.com/104885245/198347326-fd7dc957-6829-45e3-9c87-febefc60e03a.png">

* 동시에 여러 일을 할 때, 뭐가 먼저 끝나든 상관이 없을 때(순서 상관x) 먼저 응답 받은 거 보여주면 됨 아무거나
  * 예) 게임 다운 받으면서 카톡하기

**VSCODE에서 비동기** 

```
Const date = axios.get(https://~~~)
console.log(data)   //promise
```
➡️자바스크립트는 디폴트가 동기적 방식으로 작동한다.
요청하게끔 도와주는 도구들(라이브러리)은 기본적으로 비동기식으로 작동. 
자바스크립트는 위에서부터 한 줄씩 작동이 되는데 http요청이 날라가게 되고
데이터를 꺼내올 때까지 기다리지 않고 바로 아랫줄로 내려가버림
그래서 실제 데이터가 들어가있는게 아니고 언젠지는 모르겠지만 주긴 줄게의 promise 들어가있는 것이다. 

* 비동기작업을 동기로 바꿔주는 명령어: 아랫줄로 안 내려가고 기다려주는 명령어 
=>async(에이싱크, 어싱크)/await
![](https://velog.velcdn.com/images/ahk1106/post/ba271ab4-fd04-4180-b547-03d105b9eb6d/image.png)

```
Const [실행함수] = useMutation()
      createboard()      변경시키기
			(POST PUT, DELETE)
   			   useQuery 가져오기(GET)
```

**호이스팅**

* 인터프리터가 변수와 함수의 메모리 공간을 선언 전에 미리 할당하는 것
* 변수의 선언과 초기화를 분리해서 선언만 코드의 최상단으로 끌어올려 주는 것

*function 함수 선언과 var 변수 선언은 정의하는 코드보다 사용하는 코드가 앞서 등장할 수 있었고, 게다가 재선언/ 할당이 가능해지기 때문에 예기치 못한 에러 발생 
var 로 선언한 변수의 경우 호이스팅 시 undefined 로 변수를 초기화합니다.

*Const나 let도 호이스팅이 되지만, 할당되기 전에는 Temporal Dead Zone, TDZ에 있어서 앞서 등장하지 않았고 const의 경우에는 재선언/ 재할당이 모두 불가능하기 때문에 예기치못한 에러 발생을 방지

#### 📌![](https://velog.velcdn.com/images/ahk1106/post/6d2ee4b1-9a1e-4976-a9fb-2c8ee6d62801/image.png)
