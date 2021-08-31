## :octocat: _1. Git 사용법_  

</br>

> ### _1.1) git 명령어 사용법 가이드_


</br>

````bash
$ git # git 기본적인 사용 방법 가이드
````   
</br>

> ### _1.2) .git 저장소 ( Working Directory ) 생성 및 복제_   

</br>

````bash
$ git init # Local 디렉토리에 .git 파일을 생성한다.      
$ git clone # 원격 저장소(GitHub)의 폴더 및 파일을 Local에 .git 저장소를 생성한다.
````   
</br>

> ### _1.3) 사용자 계정을 등록_     

</br>
   
````bash
$ git config -g user.name "userID" # 사용자 계정을 생성한다.
$ git config -g user.email "userEmail" # 사용자 Email을 생성한다.
````   
</br>

> ### _1.4) Working Directory에서 Staging Area로 파일을 등록_   

</br>
   
````bash
$ git add "fileName" # stage area에 파일을 등록한다.
````           
</br>

> ### _1.5) Stage Area에서 Repository로 파일을 등록_   

</br>
   
````bash
$ git commit -m "logMessage" # stage area에 변화 된 파일을 commit 한다.
````
</br>

> ### _1.6) Log 정보 확인_

</br>
   
````bash
$ git log # .git의 파일 변화에 관한 Log 정보들을 알 수 있다.
````   
</br>

> ### _1.7) Branch 목록을 확인_

</br>
   
````bash
$ git branch # Branch 목록을 확인한다.
````   
</br>

> ### _1.8) Branch 생성_

</br>
   
````bash
$ git branch "branchName" # Branch 목록을 확인한다.
````   
</br>

> ### _1.9) Branch 이름 변경_

</br>
   
````bash
$ git branch -m "oldBranchName" "newBranchName" # Branch 이름을 변경한다.
````   
</br>

> ### _1.10) Branch 삭제_

</br>
   
````bash
$ git branch -d "BranchName" # Branch를 삭제한다.
````    
</br>

> ### _1.11) Branch 전환_

</br>
   
````bash
$ git checkout "BranchName" # 생성 된 Branch들을 전환한다.
````           
</br>

> ### _1.12) Branch 목록 변화 상태 확인_

</br>
   
````bash
$ git log --branches --decorate --graph # Branch의 저장 상태를 확인한다.
$ git log --branches --decorate --graph --oneline # Branch의 저장 상태를 한 줄로 확인한다.
```` 
</br>

> ### _1.13) Branch 목록 비교 변화 확인_

</br>
   
````bash
$ git log "master".."branchName" # Master와 Branch의 차이의 변화를 확인한다.
$ git log "branchName".."master" # Branch와 Master의 차이의 변화를 확인한다.
$ git diff "branchName".."master" # Branch와 Master 사이의 변화를 확인한다.
```` 
</br>

> ### _1.14) 파일 병합 ( Branch -> Master )_

</br>
   
````bash
$ git checkout "branchName" # 병합할 Branch로 전환한다.
$ git merge master # Branch의 파일을 Master로 병합한다.
````   
</br>

> ### _1.15) 파일 병합 ( Master -> Branch )_

</br>
   
````bash
$ git checkout master # Master로 전환한다.
$ git merge "BranchName" # Master의 파일을 Branch로 병합한다.
````
</br>

> ### _1.16) 파일 복원_

</br>
   
````bash
$ git reset [--option] "logCommitHash 앞 6자리" 
````
* _"--option"_ 에 따라서 파일을 복원하는 범위가 달라진다. 아래 <표>를 참고하여 _option_ 을 넣는다.
* < 표 > : _Option_ 상태    
  |   _Status_   | _Working dir_ | _Staging area_ |  _Repository_  |     
  | :--------: | :---------: | :--------:  |  :---------:  |   
  | **_Option_** | ----------- | ----------- |    _soft_     |   
  | **_Option_** | ----------- |    _mixed_    |    _mixed_    |   
  | **_Option_** |   _hard_     |    _hard_     |    _hard_     |
  
</br>
