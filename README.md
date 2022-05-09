# Today I Learned
최종수정일 : 2022.05.09

## 오늘 배운 내용



## 목차

[1. Notion](#1-notion)

[2. Git 과 Github](#2-git---github)

[3. Typora](#3-typora)

[앞으로의 계획](#-------)

[4. MacOS AWS 설정 방법](#4-macos-aws------)

+ [1번째 방법](#1-----)
+ [2번째 방법](#2-----)



---



### 	1. Notion

​		[Notion 바로가기](https://www.notion.so/)

- **노트**를 작성하고 **공유**할 수 있다.



### 	2. Git 과 Github

​		[Git 설치하기](https://git-scm.com/)

​		[Github 바로가기](https://github.com/)

#### 		깃이란?

- **분산 버전 관리 시스템**이다.
- 누가, 언제, 왜 변경했는지 알 수 있다.



##### 		깃 명령어 알아보기

- **Git - Github 연결 (User)**

  *한번만 해도 되는 작업*

​		`git config --global user.name "user_name"` : username 등록

​		`git config --global user.name` : username 확인

​		`git config --global user.email "user_email"` : email 등록

`git config --global user.name`

​		`git config --global user.email` : email 확인



- **Git - Github 연결 (Repository)**

  *Repository 연결할 때 한번만 해도 되는 작업*

  `git init` : 로컬 저장소 생성해서 git 시작

  `git remote add origin <git repository url>` : repository 연결

  `git remote` : 제대로 연결되었는지 확인할 수 있다

  

  

  **파일 수정, 생성할 때마다 해야하는 작업**

  `git add . ` : 전체 파일을 추가

  `git add README.md` : untracked인 README.md 파일을 추가

  `git commit -m '원하는 메시지 남기기'` : 커밋 메시지를 남길 수 있다 

​		`git push origin master` : 깃허브에 올리기(push)



`git log --online` : 로그 보기

`git status` : 상태를 본다



#### 		깃허브란?

- *Push, Pull*을 이용해서 파일 관리를 할 수 있다.
- **Push** : 깃허브에 파일 올리기
- **Pull** : 깃허브에서 파일 받기







### 	3. Typora

​		[Typora 설치하기](https://typora.io/)

#### 		타이포라란? 

- **마크다운 편집기**이다.
- **README.md** 파일을 통해 오픈 소스의 공식 문서를 작성할 수 있다.



##### 		타이포라 단축키 알아보기(MacOS)

`command + 1` : 헤더 1 (h1 : 제일 폰트 크기가 큰 제목, # 1개) 

`command + 2` : 헤더 2 (h2 : 1부터 6까지 순서대로 폰트 크기가 작아진다, # 2개)

`command + 3` : 헤더 3 (h3 : # 3개)

`command + 4` : 헤더 4 (h4: # 4개)

`command + 5` : 헤더 5 (h5: # 5개)

`command + 6` : 헤더 6 (h6 : 제일 폰트 크기가 작은 제목, # 6개) 



`command + option + c` : 코드 블럭

`백킷으로 감싸기`: 인라인 코드 블럭



`[string](url)` : 하이퍼링크를 생성(http까지 링크 전체가 들어가야함)

`![string](url)` : 이미지 주소 복사로 이미지 생성

`command + 클릭` : 링크 새 창이 뜬다



`command + b` : 볼드체

`command + i` : 이탤릭체

`control + shift + `(백킷)` : 취소선

`command + b + i` : 볼드체+이탤릭체



- 수평선

`-` 3개 치기

`*` 3개 치기

`_` 3개 치기



`>` : 인용문



`|` : 스페이스바 개수로 칸의 개수를 만들 수 있다



---



## 앞으로의 계획

*Notion, Typora, Github*을 이용하여 좀 더 편리하게 코딩 공부를 해야겠다.



---



## 4. MacOS AWS 설정 방법

### 1번째 방법

- 키 설정

키파일 재설정시 .ssh 디렉토리 전체 삭제해야함.
`rm -r ~/.ssh`
(./ssh 폴더 및 안의 파일 다 지우는 명령어)
`cat ~/.ssh/id_rsa.pub`
(key 확인 명령어 -> 제대로 삭제되었는지 확인)
`ssh-keygen`
(key 생성 명령어)
어느 파일에 키를 저장할지, 비밀번호는 무엇으로 할지 물어봄 -> 따로 설정하지 않고 엔터쳐서 넘기기
`cat ~/.ssh/id_rsa.pub`
(key 확인 명령어 -> 제대로 설치되었는지 확인)

- pem 파일

`cp /다운로드받은 경로/파일명.pem ~/.ssh/`
(.ssh 디렉토리에 pem파일 복사 붙여넣기)
`cd ~/.ssh`
(./ssh 디렉토리로 이동)
`ls`
(현재 디렉토리의 파일 목록을 보여주는 명령어 -> .pem 파일 생성되었는지 확인)
`chmod 600 파일명.pem`
(pem 파일 권한 변경)

- .ssh 디렉토리에서 config 파일 만들기

`vim config`
(config 파일 생성하고 `i`눌러서 다음과 같은 내용쓰기)

```
Host [서버명]
HostName [서버 접속 IP]
User [Terminal 접속 ID]
IdentityFile ~/.ssh/[키파일명.pem]
```

`esc` 누르고 `:wq!` 명령어로 저장 후 종료
`chmod 700 config`
(config 파일의 권한 수정)
`ls -l`
(파일 권한 확인하는 명령어)

- 서버접속

`ssh [서버명]`
([서버명]에 접속하는 명령어)
`yes`
입력 후 엔터

- 서버 이용 설정

`conda info - - envs`
(가상환경 목록 확인하는 명령어)
`conda activate python3`
(python3 가상환경을 실행하는 명령어)
`cat > jup`
(jup 파일 생성 명령어)
`nohup jupyter-notebook --ip=0.0.0.0 --no-browser --port=[jupyter-notebook사용 Port] &`
(입력 후 엔터치고 ctrl+d로 저장)
`chmod 777 jup`
(jup 파일 권한 변경하는 명령어)
`./jup`
(jup 파일 실행하는 명령어 -> 한번 더 엔터쳐서 넘기기)
`ps -ef | grep jupyter | grep [Terminal 접속 ID]`
(실행중인 프로세스 확인하는 명령어)

- 참고

`kill -9 [프로세스 번호]`
(프로세스가 여러 개 실행되고 있을 시에 프로세스를 강제 종료시키는 명령어 - 자신의 프로세스가 아니면 안 지워짐)

- 원격 jupyter-notebook 접속 URL로 서버접속 후에 서버 종료시 `exit` 명령어로 서버 사용 종료



### 2번째 방법



### pem파일을 다운로드 받은 폴더 안에서

`chmod 400 <키파일명.pem>`

`ssh -i <키파일명.pem> <username>@<ip주소>`



### 예시) 

`chmod 400 s-D-team01.pem`

`ssh -i s-D-team01.pem lab01@12.34.567.890`
