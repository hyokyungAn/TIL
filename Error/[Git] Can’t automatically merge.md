<img width="582" alt="스크린샷 2023-04-30 오전 12 08 34" src="https://user-images.githubusercontent.com/104885245/235309781-ba3542f6-64cb-461e-95d6-b66b9bbaa4be.png">

<img width="557" alt="image (1)" src="https://user-images.githubusercontent.com/104885245/235309381-93946152-280a-40c5-a2ab-7ed4f945a911.png">

그대로 따라해도 왜인지 다르고 안 되는 것이야아~~~ 답답한 마음에 이것 저것 만지고 다시 시도하다보니

* signin branch에서 master로 pull request를 하는 중 Able to merge가 떠야하는데 할 수 없다고 떴다; ➡️ merge pull request를 할 수가 없는 상황

구글링 시작@@

⭐️ 작업하는 동안 다른 변경사항이 생겼는데 pull 받지 않고 push 한 경우 발생!⭐️

> `git checkout master`

> `git pull`

> `git checkout 작업 중인 브랜치 이름`

> `git merge master`

순서대로 입력하면 conflict가 발생

Conflict가 발생한 파일을 열어보면,  <<<<< HEAD, ======, >>>>> master 의 표시와 함께 코드가 추가된 것을 볼 수 있다.

두 부분을 비교해서 코드를 수정하고 <<<<< HEAD, ======, >>>>> main 의 표시도 지워준다.

수정한 코드를 

> `git add 변경한 파일`

> `git commit -m`

> `git push origin 작업 중인 브랜치 이름`

이렇게 해서 해결했다!

* 공동으로 작업할 땐 웬만해선 master branch를 건드리면 안된다고 하는데 나는 다행히 혼자 따라하는 프로젝트여서 다행ㅠ.ㅠ 
