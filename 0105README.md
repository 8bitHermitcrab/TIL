# Today I Learned



## 오늘 배운 내용

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
