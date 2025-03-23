## 1. git의 정의와 github을 사용하는 이유   
* git이란? : **버전 관리 및 협업을 위해 사용하는 오픈소스 소프트웨어**    
   
* 잔뜩 쌓인 파일들을 효율적으로 관리할 수 있다.  
* 결과물의 버전 관리에 용이하다.  
* 코드의 수정을 관리하는 데에 용이하다.
    - 이슈 트래킹 : 올린 코드에 있는 에러, 이슈를 보고함   
    - 코드 리뷰 : 올린 코드를 평가, 지적함     
* 협업하여 프로젝트를 진행하는 데에 용이하다.   
    - Github actions : 코드 수정 관련 기록    
    - Github projects : 프로젝트 관련 일정 등을 관리   
--------------------------------------------------
## 2. github에 올릴 파일의 상태   
1. untracked : 파일이 추적되지 않는 상태 (git에 올리지 않은 상태)   
2. tracked : 파일이 추적되는 상태 (modified, unmodified, staged)   
    2-1. unmodified : 파일이 수정되지 않은 상태   
    2-2. modified : 파일이 작성, 수정된 상태   
    2-3. staged : 파일이 repository(local repo)로 올라가기를 대기 중인 상태   
--------------------------------------------------
## 3. github에 파일을 올리는 방법   
1. Working directory(작업을 하는 곳, 즉 일반 폴더)에서 코드를 짠다.
2. new terminal을 만들고, git bash를 한다.
3. git 최초 설정을 한다 :   
    - git config --global user.name "<깃허브 이름>" 입력   
    - git config --global user.email "<깃허브 이메일>" 입력   
4. 자신의 허브 이름과 같은 폴더를 만들고, 그 폴더를 VScode에서 openfolder를 한다.   
5. VScode에서 그 폴더 밑에 new terminal을 생성한다.   
6. .git 폴더를 만들어 디렉토리를 git 저장소로 만든다.
    - git init 입력   
7. git add를 통해 짠 코드를 저장소(repo)에 관리할 거라고 등록한다.
    + git add . 입력 : 모든 파일 한 번에 등록   
    + git add <파일명> : 파일 하나씩 등록   
    + git rm --cached < file > : unstage로 파일 되돌리기   
8. git commit을 통해 Local repo로 파일을 옮긴다.   
<<<<<<< HEAD:wil.md
    + git commit -m "< commit message >"   
=======
    + git commit -m "< 커밋 메세지 >"   
>>>>>>> 1aabd936bd8d58c1c1035c1f1a5a549dcc69b8bf:week1/wil.md
    + commit message는 다른 사람들이 내가 올린 코드를 쉽게 알아볼 수 있도록 하는 일종의 제목이다.   
9. github에 remote repository를 만든다. 이때 repository의 이름은 owner의 이름과 같게 설정한다.   
10. git push를 통해 remote repo(github)로 파일을 옮긴다.   
    + git remote add origin <주소> 입력   
    + git branch -M main 입력   
    + git push -u origin main 입력    

- 추가 용어 정리   
    + git pull : github에 있는 것들을 Working Directory로 끌고 와서 수정함   
    + git fetch : github에 있는 것들을 Local Repo로 끌고 와서 수정함   
--------------------------------------------------
## 4. github에 올린 파일을 수정하여 다시 올리기   
1. VScode에서 파일을 수정한다.   
2. git add & commit을 한다.   
3. 다음을 입력한다.   
    + git push origin main   
