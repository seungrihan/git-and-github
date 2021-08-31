#### 1.Git 사용법  
> #### git 명령어 사용법 가이드  
   
````bash
$ git # git 기본적인 사용 방법 가이드
````   
   
> #### .git 저장소 ( Working Directory ) 생성 및 복제   
   
````bash
$ git init # Local 디렉토리에 .git 파일을 생성한다.      
$ git clone # 원격 저장소(GitHub)의 폴더 및 파일을 Local에 .git 저장소를 생성한다.
````   

> #### 사용자 계정을 등록     
   
````bash
$ git config -g user.name "userID" # 사용자 계정을 생성한다.
$ git config -g user.email "userEmail" # 사용자 Email을 생성한다.
````   

> #### Working Directory에서 Stage Area로 파일을 등록
   
````bash
$ git add "fileName" # stage area에 파일을 등록한다.
````           

> #### Stage Area에서 Repository로 파일을 등록   
   
````bash
$ git commit -m "logMessage" # stage area에 변화 된 파일을 commit 한다.
````

> #### Log 정보 확인
   
````bash
$ git log # .git의 파일 변화에 관한 Log 정보들을 알 수 있다.
````   

> #### Branch 목록을 확인
   
````bash
$ git branch # Branch 목록을 확인한다.
````   

> #### Branch 생성
   
````bash
$ git branch "branchName" # Branch 목록을 확인한다.
````   

> #### Branch 이름 변경 
   
````bash
$ git branch -m "oldBranchName" "newBranchName" # Branch 이름을 변경한다.
````   

> #### Branch 삭제 
   
````bash
$ git branch -d "BranchName" # Branch를 삭제한다.
````    

> #### Branch 전환 
   
````bash
$ git checkout "BranchName" # 생성 된 Branch들을 전환한다.
````           

> #### Branch 목록 변화 상태 확인
   
````bash
$ git log --branches --decorate --graph # Branch의 저장 상태를 확인한다.
$ git log --branches --decorate --graph --oneline # Branch의 저장 상태를 한 줄로 확인한다.
```` 

> #### Branch 목록 비교 변화 확인
   
````bash
$ git log "master".."branchName" # Master와 Branch의 차이의 변화를 확인한다.
$ git log "branchName".."master" # Branch와 Master의 차이의 변화를 확인한다.
$ git diff "branchName".."master" # Branch와 Master 사이의 변화를 확인한다.
```` 

> #### 파일 병합 ( Branch -> Master )
   
````bash
$ git checkout "branchName" # 병합할 Branch로 전환한다.
$ git merge master # Branch의 파일을 Master로 병합한다.
````   

> #### 파일 병합 ( Master -> Branch )
   
````bash
$ git checkout master # master로 전환한다.
$ git merge "BranchName" # Master의 파일을 Branch로 병합한다.
````

> #### 파일 복원 
   
````bash
$ git reset [--option] "logCommitHash 앞 6자리" 
````
- "--option"에 따라서 파일을 복원하는 범위가 달라진다. 
- 아래 <표>를 참고하여 option을 넣는다.
- <표>       
  |   status   | working dir | staging area | repository |     
  | :--------: | :---------: | :--------:  | :---------: |   
  | **option** | ----------- | ----------- |    soft     |   
  | **option** | ----------- |    mixed    |    mixed    |   
  | **option** |     hard    |    hard     |    hard     |           
