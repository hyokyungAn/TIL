<img width="812" alt="스크린샷 2022-12-07 오후 4 20 52" src="https://user-images.githubusercontent.com/104885245/206123623-cd76dd69-fbe0-4358-a9b9-b08f9aee997f.png">

## 📌 SetState

<img width="1166" alt="스크린샷 2022-12-07 오후 5 26 00" src="https://user-images.githubusercontent.com/104885245/206127066-35baecf1-08e1-4a40-8ada-9b01d84ecbfd.png">

* props 넘어가는 순서

### 버튼색 변경

<img width="692" alt="스크린샷 2022-12-07 오후 5 30 41" src="https://user-images.githubusercontent.com/104885245/206128301-5db8fd1d-93f7-44cc-985a-25971c141427.png">

* 버튼이 활성화가 되는지 안되는지 ➡️ isActive

<img width="692" alt="스크린샷 2022-12-07 오후 5 34 01" src="https://user-images.githubusercontent.com/104885245/206128663-dd27cb1f-a90f-4392-82ce-d742022b3741.png">

* props를 받기 위해 함수로 만들어줘야함 ➡️ ${(props) => props.isActive ? "yellow" : "default"}
* props.isActive === true는 조건 부분(true인지 false인지 바뀌어서 실행), isActive는 이미 true이기 때문에 생략 가능
* true이면 앞에거 실행("yellow"), false이면 뒤에거 실행("default")

<img width="851" alt="스크린샷 2022-12-07 오후 5 46 13" src="https://user-images.githubusercontent.com/104885245/206131502-1a330824-c44f-4db0-b8c6-e72b37899ab5.png">

* isActive={true}처럼 하드코딩을 할 수도 있지만 변수에 담아서 보내줄 수도 있음
* container에서 state를 만들어줌, 초기값 false ➡️  const [isActive, setIsActive] = useState(false)

<img width="1080" alt="스크린샷 2022-12-07 오후 5 41 19" src="https://user-images.githubusercontent.com/104885245/206132130-1d431ade-c9cb-421f-ad5a-e5d1e68d8363.png">

* isActive state를 props로 넘겨줌 ➡️ isActive={isActive} → props → isActive={props.isActive}
* 최종적으로 props.isActive는 false를 의미!!

<img width="846" alt="스크린샷 2022-12-07 오후 6 15 34" src="https://user-images.githubusercontent.com/104885245/206178399-a30f02c6-a492-4ff5-872b-4b75ceccf58e.png">

* 모든 칸이 입력 완료되면 버튼색이 바뀜 ➡️ if(writer && title && contents){setIsActive(true)}
* 어떤 input창이 마지막에 입력될지 모르기 때문에 모든 input에 넣어줘야함

<img width="843" alt="스크린샷 2022-12-07 오후 6 33 14" src="https://user-images.githubusercontent.com/104885245/206142470-85603468-0ba5-4647-a8d3-fc5948ac9160.png">

* 작성자에 ㅊ을 입력하는 순간 OnChangeWriter가 실행됨 → event에 입력된 태그가 들어오게 되고 event.target하면 input태그가 들어옴 → .value하면 ㅊ이 들어옴 ➡️ event.target.value: ㅊ

<img width="526" alt="스크린샷 2022-12-07 오후 6 32 07" src="https://user-images.githubusercontent.com/104885245/206179474-a022f7eb-72bc-4d54-813c-51b11198b873.png">

* setWriter를 등록하게 되면 state인 writer가 ㅊ이 됨, 그러나 if 조건문의 writer는 ㅊ이 아님! ➡️ 빈문자열""

<img width="747" alt="스크린샷 2022-12-07 오후 9 31 40" src="https://user-images.githubusercontent.com/104885245/206180093-1426cd24-31d3-430f-9a2b-63a014befd93.png">

* setState에 값을 넣게되면 바로 writer가 변하는 것이 아닌 임시저장공간에 writer를 ㅊ으로 바꿔줘라고 해놓음 → 함수가 끝나면 임시저장공간에 있던 내용이 실제로 반영이 돼서 writer가 ㅊ으로 바뀜

🙋🏻‍♀️ 왜 함수가 끝났을 때 변경이 되는지?

* 여러 개의 setState가 존재할 경우 버튼을 클릭하고 setState 수만큼 리렌더링이 일어나면 굉장히 비효율적
* 그 문제점을 해결하기 위해 임시저장공간에 변하는 값을 저장해뒀다 끝나면 마지막 결과가 최종적으로 1번만 리렌더링됨

<img width="587" alt="스크린샷 2022-12-07 오후 9 37 53" src="https://user-images.githubusercontent.com/104885245/206181227-1a05dce8-4c66-4f0e-aaab-5b313a70795f.png">

* state가 ㅊ으로 바뀌게 되면 그 state를 사용하고 있는 컴포넌트가 새롭게 다시 만들어짐 ➡️ 리렌더링(렌더링이 됐던 컴포넌트가 다시 렌더링 되는 것 - 비효율적 → 재바인딩
* use로 시작되는 훅은 유지되고 콘솔, 변수, 함수, return 부분이 다시 만들어짐  
 
<img width="364" alt="스크린샷 2022-12-07 오후 9 49 42" src="https://user-images.githubusercontent.com/104885245/206183731-f91900e1-ac97-4ebe-a2f0-7d9fb36b58d0.png">

* setWriter를 바꿔도 if문의 writer는 아직 빈문자열이기 때문에 함수가 끝나야 바뀜 ➡️ writer를 event.target.value로 바꿔줘야 함

<img width="852" alt="스크린샷 2022-12-07 오후 9 53 35" src="https://user-images.githubusercontent.com/104885245/206184664-bad44acb-aa1b-4371-b3fe-ff4082686642.png">

* 다시 빈칸이 생겼을 때 버튼색이 원래대로 돌아오게 해줌 ➡️ setIsActive(false)
