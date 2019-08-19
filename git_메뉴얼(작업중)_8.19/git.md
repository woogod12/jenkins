**Git 메뉴얼**
===
## **1. GIT 소개**
  + ### GIT 이란?
    + 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템.
  + ### SVN과 차이점
    + 로컬저장소와 원격저장소의 분리가능<br>
    -> 분산 처리, 안전한 데이터, 빠른 처리 속도
    + 스테이지 영역의 존재<br>
    -> 커밋 대상의 분리
    + 스냅샷을 이용한 버전 관리<br>
    -> 빠르고 편리한 브랜치 & 병합 기능
---
## **2. Git 시작하기**
+ ### git 설치    
  * http://msysgit.github.com/ 
  * 설치완료후 GIT 폴더로 가서 'git-bash.exe'를 실행합니다.
    ![설치2](./실행화면.png)
    -> 위 화면이 실행되면 git 설치 완료입니다.

+ ### git 환경설정
  + git config 설정  
    + 사용자 설정 git을 commit할때 입력되는 사용자의 이메일과 이름 정보를 등록합니다.<br>
      ``` 
      git config --global user.name 'name'
      git config --global user.email example@gmail.com
      ```
    + 주로 사용할 텍스트 편집기를 입력합니다.

          git config --global core.editor (편집기이름)

    + git config 설정 확인을 통해 user.name과 email을 확인합니다.

          git config --list

---
## **3. Git 저장소 만들기**
  + ### git init
    + 'init 명령어는 해당 디렉토리를 git 레파지토리로 만들어 줍니다.  
    ls -al 명령어를 입력하면 .git 파일이 생성된것을 확인할 수 있습니다.
    ![초기3](./init.png)
  + ### git clone
    + git clone 명령을 실행하면 프로젝트 히스토리를 전부 받아옵니다.   

          git clone (가저올 저장소 url)

---
## **4. Git 수정하고 저장소에 저장하기**

  + ### git status
    + 파일의 상태를 확인하는 명령어로 처음 실행하면 아래와 같은 메시지가 나온다.  

          git status
          On branch master
          nothing to commit, working directory clean

  + ### git add
    + git add 명령으로 파일을 새로 추적합니다.  

          git add (추적할파일)  

    + git add를 한후 git status 명령을 다시 실행하면 (추적할파일)이 Tracked 상태이면서 Staged 상태라는 것을 확인 할 수 있습니다.

          git status
          On branch master
          changes to be committed:
            (us "git reset HEAD ..." to unstage)

                new file: (추적할파일)

         
  + ### git commit
    + 커밋을 실행하면 변경된 파일이 HEAD에 반영됩니다.

           git commit -m "변경된 메시지 내용 입력"  
    + git add 명령 실행 이후에 수정한 파일까지 한번에 커밋하기 위한 명령어 
    
          git commit -am "커밋 메시지 내용"
 
  + ### git log
    + git log 명령을 통해 버전이 기록됨을 확인 할 수 있습니다. 
    ![log](./gitlog.png) 
---
## **5.Git remote 저장소**
  + ### git remote
    + 원격 저장소를 이용하기 위해 git 에게 아래 명령어로 원격 서버의 주소를 알려줍니다.

          git remote add origin <원격 서버 주소>
        -> 여기서 origin은 원격저장소의 별칭입니다.

  + ### git push
    + 최신 커밋 사항을 git repository에 올리기 위해서 사용하는 명령어 입니다.

          git push - u orgin master

        -> 여기서 - u 는 원격저장소로부터 업데이트를 받은후 push를 한다는 의미입니다.
         
---
## **6. Git branch**
  + ### 브랜치란?
  + ### git branch
  + ### git merge
---
## **7. Git 기타명령어**
  + ### git commit --amend
  + ### .gitignore
  + ### git diff 설정 
   + git diff는 커밋후 변경된 사항을 보여주는 명령어 입니다.
    + git diff tool 설정을 위해 git kDiff3 설치 설정 법을 예시로 들겠습니다.
---
## **8. Tips & Etc**
  + ### 이슈해결
     + git 초기설정 오류시 전체 초기화 방법
   ![clean](./clean.png)

       > git clean -i 명령어를 수행하고 c를 입력하면 전체 초기화를 실행합니다.

  + ### Github 연동
    + GitHub에 로컬에서 만든 git을 저장하기 위해서는 GitHub의 계정을 만들고 저장할 repository가 필요합니다. 계정과 repository를 생성해주세요.

      ![hub](./github.png)
      > + 생성한 GitHub repository로 로컬 git 연결을 위해 remote add 명령어를  사용합니다. 여기서 origin은 원격저장소의 별칭입니다.  

      ![push](./gitpush.png)
      > + git push 명령어를 통해서 로컬저장소와 원격저장소를 동기화 시켜줍니다.
      완료되었으면 github의 자신이 생성한 repository에 로컬에서 생성한 파일들이 업로드 되어 있음을 확인할수 있습니다.

      ![re](./gitre.png)  

--- 
  



     








