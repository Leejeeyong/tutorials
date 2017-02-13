Git init

directory: workbench

$ git init # 저장소 초기화  .git 디렉토리 생성(깃파일 생성과 변경이력 보관)


# 사용자 이름 이메일 등록

$ git config --global user.name "Leejeeyong"
$ git config --global user.email "fghj0720@gmail.com"
$ git config --local user.name "Leejeeyong"
$ git config --local user.email "fghj0720@gmail.com"
$ git config -l

# 디렉토리에  파일 추가

$ git status
$ git add content.docx
$ git add . # 변경 사항만
$ git add *.docx # docx의 확장자를 가진 파일들만

.gitignore # 제외하고싶은 파일 설정
ex) contents: ~*.* # 임시파일 제 외

# 추가 되돌리기(option)

$ git reset filename.extension

# 파일 커밋(새로운 단계 규정)

$ git commit -m "your comments for the commit"

# 체크 아웃(이력간의 이동)

$ git log # 저장소 이력
$ git check ___commit_id___

$ git checkout master #최근변경사항으로 되돌림

# git 실핼명령 패턴

$ git operation_keyword parameter and/or values

 git clone # 깃의 복제
 git fetch # 소스부터 목적지까지 변경사항
 git merge # 분기를 하나로 합침
 git push # 소스를 목적지에 밀어넣음
 git remote # 소스와 목적지를 관리(fetch, push, pull)

# 저장소에 원격지의 origin을 연결하거나 추가하는 방법

$ cd /path/to/wokbench
$ git remote add origin http://your_github_id/online_workbench.git
$ git push -u origin master

# 다른 곳에서 작업

$ git clone https://-/-/-.git/path/workbench
$ git add *
$ git commit -m "your commit message"
$ git pull
$ git push

# 노출된 저장소 생성

$ git clone --bare c:/user/workbench c:/share/bare_workbench
