---
title: "[JavaScript] Node.js 환경 구축 (with. VSCode)"
excerpt: "node.js 설치와 nodemon 사용 방법"

categories:
  - javascript
tags:
  - [javascript, 자바스크립트기초]

permalink: /categories/javascript/2

toc: true
toc_sticky: true

date: 2024-11-10
last_modified_at: 2024-11-10
---

## 🦥 본문

<br>


자바스크립트를 웹브라우저가 아닌 로컬에서 바로바로 실행해보자

### Node.js

🔗[https://nodejs.org/en](https://nodejs.org/en)

- 위의 링크에서 해당 프로그램 다운받아서 실행
- 컴퓨터 언어인 JavaScript를 사용해서 컴퓨터 프로그램을 만들 수 있게 해주는 도구이다.
- JavaScript는 웹 브라우저 안에서만 자바스크립트  엔진을 통해 동작하는데, Node.js를 이용하면 컴퓨터(로컬) 에서도 동작이 가능하다.
- 설치 후에는 윈도우 어느곳에서도 사용이 가능하다

<br>

### nodemon

Nodemon은 Node.js로 실행하는 파일을 자동으로 감시하는 도구이다. 파일이 변경되면 Nodemon이 서버를 자동으로 재시작해 변경 사항을 즉시 반영할 수 있게 해준다. 이를 통해 개발자는 코드 수정 후 매번 수동으로 서버를 재시작할 필요 없이 더 빠르고 효율적으로 작업할 수 있다.

<br>

### npm

🔗 [https://www.npmjs.com/](https://www.npmjs.com/)

자바스크립트 유저들이 만든 가장 큰 오픈소스 사이트이다.

다양한 라이브러리 및 패키지를 쉽게 설치하고 관리할 수 있다.

`nodemon` 최신 버젼 등이 있다. 

---

<br>
<br>

### vscode에서 nodemon 사용법과,  주요 명령어

1. node.js 설치 후 진행
2. **상단 메뉴  → Terminal → New Terminal** 
    
    (vscode에서 사용가능한 cmd창이다. 단축키 : `ctrl+ shift + `` )
    
3. **node.js 버젼확인**
    
    ```bash
    node -v
    ```
    
4. **nodemon 설치**
    
    ```bash
    npm install -g nodemon
    ```
    
5. **nodemon 실행**
    
    ```bash
    C:/path/to/your/project> nodemon project3.js
    ```
    
    - nodemon을 실행할 프로젝트 폴더로 이동 후 (`cd`) 실행할 파일을 찾아서 실행한다.

6. **nodemon 사용 종료** 단축키 : `ctrl + c` 


<br>
<br>