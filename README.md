## 📝 Content
### **[1. _Git_ 사용법](#1.Git-사용법)**   
&nbsp;&nbsp;[1-1) _Git_ 명령어](#Git-명령어)      
### **[2. _GitHub_ 사용법](#2.GitHub-사용법)**      
&nbsp;&nbsp;[2-1) _GitHub_ 명령어](#GitHub-명령어)   
  
## 1.Git 사용법   
  - ### Git 명령어   
  
    - **_Git_ 의 명령어의 사용법을 보고 싶다.**   
           
       <code>$git</code> : 명령어의 사용법을 알고 싶다.  
    
    - **저장소를 생성하거나 원격저장소에서 _Local_ 디렉토리에 복제 하고 싶다.**   
        
       <code>$git init</code> : _**Local**_ 에 _**git**_ 저장소를 생성한다.   
       <code>$git clone</code> : **원격저장소**(_**GitHub**_)의 폴더 및 파일을 _**Local**_ 에 _**git**_ 저장소를 생성한다.   
          
    - **사용자 및 Email을 등록하고 싶다.**   
       
       <code>$git config -g user.name "userId"</code> :  _**사용자계정**_ 을 생성한다.   
       <code>$git config -g user.email "userEmail"</code> :  _**사용자 Email**_ 을 생성한다.   
          
    - **저장소의 상태 변화를 알고 싶다.**   
         
       <code>$git status</code> : 저장소의 상태 변화를 알고 싶다.   
          
    - _**Stage Area**_ **에 파일을 등록 한다.**   
       
       <code>$git add "fileName"</code> : _**Stage Area**_ 에 파일을 등록한다. _( Untrack -> track )_
    
    - **_Stage Area_ 의 변화된 파일을 _commit_ 한다.**   
        
       <code>$git commit -m "logMessage"</code> : _**Stage Area**_ 에 변화된 파일을 _**commit**_ 한다. _( track -> Untrack )_
  
    - **_Local_ _git_ 저장소의 변화된 파일의 _Log_ 들을 확인 한다.**   
       
       <code>$git log</code> :  변화 파일들의 상태 변화를 알고 싶다.   
          
    - **_Local_ _git_ 저장소의 변화된 파일의 특정 시점으로 돌아가고 싶다. ( !복구불가능 )**    
           
       <code>$git reset "일련번호6자리" or "logCommitHash" --hard</code> : 특정 시점으로 돌아가고 싶다.    
 
