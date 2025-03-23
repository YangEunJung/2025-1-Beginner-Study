GDG 개발 입문 스터디 1주차 wil     
==============================

# 1. 개발의 중요성

1. 코드의 수정을 관리해야 한다. / 버전 관리가 필요하다.

    코드가 수정되었을 때, 따로 저장할 경우 번거로울 수 있다.
    또한, 새로운 기능을 만들어 배포했을 때 이후 문제가 생긴다면
    이전 버전을 기용함으로써 일시적으로 문제를 해결할 수 있는데,
    깃을을 활용하면 이전 버전을 사용하는 것이 용이하다.

  
2. 잔뜩 쌓인 파일을 관리해야 한다.

    이후 프로젝트에 참여하면서 수많은 파일을 관리하게 되는데, 
    수많은 파일을 편리하게 관리하기 위해선 깃을 활용하는 것이 좋다.


3. 개발은 혼자하는 것이 아니다.

    규모가 큰 프로젝트일수록 여러 개발자와 함께 작업하게 된다.
    이때 파일을 항상 이메일이나 usb를 통해 전달하는 것은 매우 불편할 것이다. 따라서 깃을 활용하는 것이 좋다.



# 2. Git이란?

Git은 버전 관리 및 협업을 위해 사용하는 오픈소스 소프트웨어이다.
어떤 파일이 / 언제 / 누가 / 어떻게 수정했는지 추적하는 데 용이하다. 


# 3. 파일의 생명주기

1. Untracked

    일반적으로 어떠한 절차도 거치지 않은 파일은 대부분 Untracted 상태이다.
    반대로 깃에 파일을 등록하면 파일은 tracked 상태가 된다.


2. Unmodified

    파일일을 add하면 Untracked상태에서 Unmodified 상태가 된다.


3. Modified

    Unmodified 상태의 파일에서 수정을 거치면 Modified 상태가 된다.


4. Staged

    Mmodified 상태의 파일을 stage하면 Staged 상태가 된다.
    Staged 상태의 파일을 Commit하면 다시 Unmodified 상태로 돌아간다.



# 4. Git의 영역

1. Working Directory

    일반적으로 local 즉, 작업 중인 컴퓨터 내의 폴더를 이야기 한다.
    git add 행위를 통해서 Staging Area로 넘어간다.


2. Staging Area

    staged 상태의 파일이 있는 장소이다.
    git commit 행위를 통해서 Repository로 넘어간다.


3. Repository

    (Local 레포지토리의 경우) commit된 파일이 머무는 장소이다.
    git push 행위를 통해 Remote Repository(쉽게 말하자면 git hub)로 넘어간다.
    git petch 행위를 통해 Remote -> Local 방향으로의 이동도 가능하다.



# 5. Git으로 파일 관리하기

1. 디렉토리에 Git 저장소 만들기

    Git init 명령어를 활용한다.


2. Git으로 관리할 대상 등록하기

    git add 명령어를 활용한다.
    git add . <<모든 파일을 한 번에 등록
    git add <파일명> <<원하는 파일을 하나씩 등록


3. 파일 수정 후 로컬 저장소로 옮기기

    git commit 명령어를 활용한다.
    git commit -m "<commit message>" 



## 5.5. commit message

깃과 깃허브는 위에서 서술했다시피 타인과의 협업 역시 주된 목적이므로,
한눈에 알아보기 쉽도록, 또 commit messege만 보고도 어떤 내용을 수정했는지 이해할 수 있도록 작성해야 한다.

"type: subject" 형식으로 적는 것이 일반적.
예: docs: 자기소개서 초안을 작성함.

    * feat: 새로운 기능을 추가한 경우
    * refactor: 기존 코드를 개선한 경우
    * fix: 버그를 수정한 경우
    * chore: 코드 외의 설정을 바꾼 경우
    * docs: 문서화
    * test: 테스트 코드


# 6. GitHub에 올리기

$ git add <파일명명>
$ git commit -m "<commit message>"
$ git push origin main 
