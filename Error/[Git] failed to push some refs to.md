<img width="589" alt="스크린샷 2023-04-29 오후 11 43 21" src="https://user-images.githubusercontent.com/104885245/235308767-6e310a9f-0468-41c2-8876-1052934cb390.png">

* git push를 하는데 에러 발생!

혼자 공부할 때 에러가 나오면 넘 당황스럽지만 일단 구글 검색... 역시 나와 같은 상황을 겪는 사람들이 많다ㅠㅠ

찾아보니 ⭐️내 컴퓨터(local)에는 존재하지 않는 파일이 원격저장소(github)에 존재할 때 push를 진행하면 발생한다⭐️고 한다~!!

* github에서 내컴퓨터로 pull 명령어를 실행한 후 다시 push를 진행하면 해결!

> `git pull origin master`

> `git push origin master`

master로 해야하는지 signin으로 해야하는지 헷갈렸는데 git push origin signin으로 해도 해결이 되었다... 헷갈려😮‍💨 흠흠
* github에서 내컴퓨터로 pull 명령어를 실행한 후 다시 push를 진행하면 해결!
