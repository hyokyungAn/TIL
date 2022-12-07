<img width="812" alt="스크린샷 2022-12-07 오후 4 20 52" src="https://user-images.githubusercontent.com/104885245/206123623-cd76dd69-fbe0-4358-a9b9-b08f9aee997f.png">

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

* 하드코딩을 할 수도 있지만 변수에 담아서 보내줄 수도 있음
* container에서 state를 만들어줌, 초기값 false ➡️  const [isActive, setIsActive] = useState(false)

<img width="1080" alt="스크린샷 2022-12-07 오후 5 41 19" src="https://user-images.githubusercontent.com/104885245/206132130-1d431ade-c9cb-421f-ad5a-e5d1e68d8363.png">

* isActive state를 props로 넘겨줌 ➡️ isActive={isActive} → props → isActive={props.isActive}
* 최종적으로 props.isActive는 false를 의미!!

* 모든 칸이 입력 완료되면 버튼색이 바뀌고 다시 비워지면 원래대로 돌아옴
* 어떤 input창이 마지막에 입력될지 모르기 때문에 모든 input에 

<img width="843" alt="스크린샷 2022-12-07 오후 6 33 14" src="https://user-images.githubusercontent.com/104885245/206142470-85603468-0ba5-4647-a8d3-fc5948ac9160.png">

* ㅊ을 입력하는 순간 
