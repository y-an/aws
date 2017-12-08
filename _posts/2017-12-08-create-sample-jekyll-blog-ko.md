지킬 블로그 만들기
======

참고: 아래 글은 현재 진행 형입니다. 

{:toc}

시작하기
------
새로운 배움을 정리하기 위한 공간을 위한 조건:
1. Markdown 을 쓸 수 있을 것 
2. 사이트 변경에서 부터 소유권 및 저작권에 있어 자유도가 있을 것
3. 무료 였으면
4. 컴퓨터에 그 어떤 것도 설치하지 않아도 될 것 (git, ruby, jekyll)
5. 새로운 주제의 블로그를 만들때 fork 와 함께 1분만에 만들고 혹은 버릴 수 있을것
6. 어디서든지 글을 작성 및 수정 할 수 있을 것. (안드로이드의 MGit 클라이언트나 github 웹페이지에서)

따라하기
------
사용자 이름이 "블로거" 라는 가정하에 설명합니다. 

### 블로거.github.io 주소로 하고 싶을 경우
1. 다음을 포크한다. 저장소 (Repository) 이름: 블로거.github.io
2. _config.yml 파일을 열어서 수정한다
** baseUrl 삭제

### 블로거.github.io/blog 주소로 하고 싶을 경우
1. 다음을 포크한다. 저장소 이름: blog
2. _config.yml 파일을 열어서 수정한다
** baseUrl을 blog 로 변경


결과물
------
총 11 KB, 60줄 (sloc, source lines of code)로 블로그 생성 가능. 포크 후 아래 다섯 파일만 있으면 기본 블로그가 만들어진다. 
1. _posts/2017-01-31-hello-world.md (예제 포스트)
2. _layouts/default.html (HTML 레이아웃) 33 sloc,  10.6 KB
3. _layouts/post.html (글 레이아웃) 7 sloc,  122 Bytes
4. _config.yml (지킬 설정 파일) 6 sloc, 164 Bytes
5. index.html (목록 및 시작 페이지) 14 sloc, 264 Bytes

글쓰기
------
github 웹페이지에서 "_posts" 폴더 안에 2017-01-31-subject.md 파일을 만들어주고 마크다운형식으로 글을 작성한다.

옵션사항
------
1. Google Analytics 설치하기 (초기에는 필요 없음)
1. (댓글 서비스가 필요하다면) Disqus 설치하기 
1. Google Search Console에 등록하기 (정보 공유가 목적이 아닐 경우 필요 없음)
1. [각주 달기](http://sherifsoliman.com/2014/11/07/Bigfoot-in-Jekyll/)
