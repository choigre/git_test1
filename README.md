# 마크다운 사용법 익히기
*** 
처음에 임시폴더에서 마우스 우클릭을 하여 git Bash를 실행한다   
git init => repository 초기화   
git add . => 스테이지 영역에 올리기 (commit 전 임시영역)   
git commit -m "커밋 메시지 한줄"   
git commit 이후 여러줄 입력하기위한 에디터 등록하려면   
git config --global core.editor "\에디터경로"   
에디터 설정후 git commit 실행하면 에디터가 실행되고 커밋메시지 입력후 현 편집창을 닫으면 커밋이 자동 실행됨   
git status => repository 상태확인   
git log 변경여부 확인 (현재 브랜치 로그 확인)   
git log --graph 그래프 형태로 로그 확인   
git log --pretty=short 날짜가 생략된 채 로그 확인 
git log -p 변경내용 확인  
git reflog (현재 repository 전체 로그 확인)   
git diff 
git diff HEAD (최신 커밋과의 차이 확인)
***   
원격 repository 새로운 저장소를 만들고   
로컬 repository의 파일을 원격으로 보내려면   
git remote add origin 원격git주소 (origin이라는 식별자가 원격git주소를 가리킴)   
git push -u origin master (-u 지정시 로컬 repository의 현재 브랜치의 상태값이 원격 repository의 master 브랜치로 설정)  
원격 repository에서 로컬로 가져올때는   
git clone 원격git주소   
***
git bash 입력을 모두 지울때는 clear   
***
## 브랜치 생성
* git branch 현재 어떤 브랜치를 사용하는지 확인
* git checkout master(or 브랜치명) 현재 브랜치를 master(or 브랜치명)으로 이동
* git checkout -b 브랜치명 브랜치명을 새로 만들어서 그곳으로 이동
    * 새로운 브랜치명을 만들고 파일 변경후 push 를 하면 안올라감
    * 반드시 새로운 브랜치명을 master에 merge한 이후에 push해야 원격에 반영됨
    * merge 명령어를 입력하면 commit 입력 편집창이 열리고 커밋메시지 입력후 편집창을 닫으면 자동으로 커밋이 됨
    * git checkout master (master로 이동후에 merge를 수행해야함)
    * git merge --no-ff 새로운브랜치명
### 과거 상태로 복원
+ git log --graph 복원하고싶은 지점을 확인 (F2를 누르면 입력창으로 빠져나옴)
+ git reset --hard 복원하고싶은해시값
***
git commit --amend 직전 커밋메시지 변경할때   
git rebase -i HEAD~2 최신 커밋(HEAD)을 포함한 2개의 변경내역 에디터 표시
- fixup 커밋 로그를 삭제

