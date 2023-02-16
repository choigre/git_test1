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
git log 변경여부 확인 (현재 브랜치에서만 확인)   
git log --graph 그래프 형태로 로그 확인   
git log --pretty=short 날짜가 생략된 채 로그 확인 
git log -p 변경내용 확인  
git reflog (전체 로그 확인, 현재 브랜치가 아닌)   
git diff 
git diff HEAD (최신 커밋과의 차이 확인)
***   
원격 repository 새로운 저장소를 만들고   
로컬 repository의 파일을 원격으로 보내려면   
git remote add origin 원격git주소 (origin이라는 식별자가 원격git주소를 가리킴)   
git push -u origin master (-u 지정시 로컬 repository의 현재 브랜치의 상태값이 원격 repository의 master 브랜치로 설정)   
***
git bash 입력을 모두 지울때는 clear   
***
## 브랜치 생성


