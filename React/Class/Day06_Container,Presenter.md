## Optional-Chaining vs Nullish-coalescing

* Optional-Chaining: 조건부 렌더링(화면에 그리기)을 도와주는 연산자로 다른 조건부 렌더링 연산자를 더욱 간결하게 만들어서 사용하기 위해 탄생(ES11문법)

1. 삼항 연산자
2. && 연산자
3. 옵셔널 체이닝(optional-chaining)

* Nullish-coalescing: 옵셔널 체이닝 처럼 많이 사용하는 것은 아니지만, 같은 ES11문법에서 나온 앞에가 null과 undefined일때만 렌더해주는 연산자

## Container, Presenter

<img width="788" alt="스크린샷 2022-12-05 오후 10 34 05" src="https://user-images.githubusercontent.com/104885245/205660914-4cddec20-0659-4302-bc6a-cde2ea702941.png">

* 하나의 컴포넌트, 페이지 컴포넌트일 수도 있고 아닐 수도 있음(각각의 컴포넌트들을 조립해서 하나의 페이지가 만들어짐)
* 페이지 컴포넌트: pages/ 안에 있는 컴포넌트

<img width="891" alt="스크린샷 2022-12-05 오후 10 35 50" src="https://user-images.githubusercontent.com/104885245/205660944-180de2a4-ccf9-49d9-b10c-0de979fac90d.png">

* .js는 확장자를 의미하는 .으로 중요!
* 왜 잘게 쪼개야하는가? - 한 페이지에 너무 많은 코드가 있을 경우 에러난 부분을 찾기가 힘들어짐, 한 파일에 소스코드를 짧게 쓰기 위해 ➡️ 유지 보수가 좋은 코드를 만들어야 함
* 가급적 한 페이지에 코드는 70줄정도, 최대 100줄 

<img width="1021" alt="스크린샷 2022-12-05 오후 10 40 28" src="https://user-images.githubusercontent.com/104885245/205660965-5f82d33c-2267-4f50-89f7-975bf61b0098.png">

* 실제로 실행할 때 두개의 컴포넌트가 하나로 합쳐짐 ➡️ 자식이 부모 위치로 들어가서 하나로 합쳐져서 실행
* 컴포넌트 간에는 부모와 자식이 존재함

### props: 부모 컴포넌트가 자식 컴포넌트에게 물려주는 변수/함수

<img width="975" alt="스크린샷 2022-12-05 오후 11 46 45" src="https://user-images.githubusercontent.com/104885245/205665954-50d4d3e1-64cb-4054-a3fe-7805a70dd763.png">

* aaa={handleChangeWriter} 부분에 아무 값이나 원하는대로 입력 → **props라는 객체로 변함, key가 aaa, value가 handleChangeWriter로 들어감**
→ presenter 컴포넌트의 props라는 곳으로 전달 → props에는 aaa가 들어있음 ➡️ props.aaa는 handleChangeWriter가 됨

<img width="326" alt="스크린샷 2022-12-06 오전 12 06 26" src="https://user-images.githubusercontent.com/104885245/205670870-024724e8-ece4-4000-9e4d-884c69cfd3d4.png">

* 밖에 있는 commons는 여러 컴포넌트나 페이지에서 사용되는 함수같은 것들
* commons와 units는 둘다 컴포넌트로 commons는 두 번 이상 반복적으로 쓰이는 컴포넌트, units는 한 번만 쓰이는 컴포넌트

⭐️ 리액트에서 데이터 흐름은 **단방향 구조**(흐름 명확), 부모에서 자식으로밖에 데이터가 못 내려감, 자식 → 부모 ❌ 
