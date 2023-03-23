# 202030223 이강현
학교 React1 과목 공부한 내용들
<br><br>

## 2023.03.23 4주차<br>
1. 1교시<br>

> * ### 새 프로젝트 만들기 
>   1. README.md 백업
>   2. 23-react1 폴더 삭제/이름변경
>   3. 새 프로젝트 생성(23-react1)
>   4. GITHUB 저장소 삭제
>   5. 23-react1 push
>   6. GITHUB 저장소 확인
>   7. README.md 파일 복원
>   8. create-react-add 23-react1 및 npm start

2. 2교시<br>

> * ### 3.1 JSX란?
>   * JavaScript에 XML을 추가한 확장 언어다.
> * ### 3.2 JSX의 역할
>   * JSX는 내부적으로 XML/HTML 코드를 자바 스크립트로 변환한다.
>   * React가 createElement함수를 사용하여 자동으로 자바스크립트로 변환해준다.
>   * 만일 JS작업할 경우 직접 createElement함수를 사용해야 한다.
>   * JSX는 가독성을 높여주는 역할을 한다.
> * ### 3.3 JSX의 장점
>   * 코드가 간결해 진다.
>   * 가독성이 향상 된다.
>   * Injection Attack이라 불리는 해킹 방법을 벙어함으로써 보안에 강하다.

3. 3교시<br> 

> * ### 3.4 JSX 사용법
>   * 모든 자바스크립트 문법을 지원한다
>   * 자바스크립트 문법에 XML과 HTML을 섞어서 사용한다.
>   * 만일 HTML이나 XML에 자바스크립트 코드를 사용하고 싶다면 {}괄호를 사용한다.
> * ### (실습) JSX 코드 작성해 보기
>   * create-react-app으로 만든 프로젝트를 VSCode로 연다.
>   * src 디렉토리에 'chapter_03'이라는 디렉토리를 생성한다.
>   * 생성한 디렉토리에 Book.jsx라는 파일을 생성한다.

## 2023.03.16 3주차<br>
1. 1교시<br>

> * ### 0.4 개발 환경 설정하기
>   * node.js 설치하기 <br>(ps. 패키지를 설치 했을때 버전 확인하는 습관을 들여놓기)
>   * node --version (node -v)
>   * npm --version (npm -v)
>   * npx --version (npx -v)
<br>

2. 2교시<br>

> * ### 1.1 리액트는 무엇인가?
>   * 리액트의 정의
>       * 사용자 인터페이스를 만들기 위한 자바스크립트  라이브러리
>       * 라이브러리란?<br>
            자주 사용되는 기능을 정리해 모아 놓은 것
>   * 다양한 자바스크립트 UI 프레임워크
>       * Stack Overflow trands <br>
            (UI 프레임워크를 모아서 어떤 것이 인기가 많은지 보여주는 사이트)
>   * 리액트 개념 정리
>       * 복잡한 사이트를 쉽고 빠르게 만들고, 관리하기 위해 만들어진 것
>       * 다른표현으로는 SPA를 쉽고 빠르게 만들 수 있도록 해주는 도구
> * ### 1.2 리액트의 장점
>   * 빠른 업데이트와 렌더링 속도
>       * 이 것을 가능하게 하는 것이 바로 Virtual DOM이다.
>       * DOM(Document Object Model)이란 XML, HTML 문서의 각 항목을 계층으로 표현하여 생성, 변형, 삭제할 수 있도록 돕는 인터페이스. W3C의 표준이다.
>       * Virtual DOM은 DOM 조직이 비효율적인 이유로 속도가 느려서 고안된 방법이다.
>       * DOM은 동기식 Virtual DOM은 비동기식 방법으로 렌더링 한다. <br> (ps. 비동기식이 발전 할 수 있었던 이유는 개발할때 모바일을 먼저 설계한 뒤 데스크탑을 그 다음으로 개발하는 모바일 중심으로 변경되어서(아마도))
>   * 컴포넌트 기반 구조
>       * 리액트의 모든 페이지는 컴포넌트로 구성됨
>       * 하나의 컴포넌트는 다른 여러 개의 컴포넌트의 조합으로 구성 가능
>       * 리액트로 개발 하다 보면 레고 블록을 조립하는 것처럼 컴포넌트를 조합해서 웹사이트를 개발하게 된다.
>       * 이런 방식은 재사용 성이 뛰어나다.
>   * 재사용성
>       * 반복적인 작업을 줄여주기 때문에 생산성을 높여준다.
>       * 유지보수가 용이하다.
>       * 재사용이 가능하려면 해당 모듈의 의존성이 없어야 한다.


3. 3교시<br>
> * ### 1.2 리액트의 장점
>   * 든든한 지원군<br>메타(구 페이스북)에서 오픈소스 프로젝트로 관리하고 있어 계속 발전하고 있다.
>   * 활발한 지식 공유 및 커뮤니티
>   * 모바일 앱 개발 가능
> * ### 1.3 리액트의 단점
>   * 방대한 학습량<br> 자바스크립트를 공부한 경우 빠르게 학습이 가능하다.
>   * 높은 상태 관리 복잡도<br> state, component life cycle 등의 개념이 있지만 그리 어렵지 않다.
> * ### 2.3 (실습) 웹사이트에 React.js 추가하기
>   * 간단한 리액트 컴포넌트를 만든다. like_button.js
>   * 그리고 index.html을 실행한다.
>   * 버튼이 보이는지 확인한다.
>   * 버튼을 누르면 Clicker! 라고 뜨는지 확인한다.
> * ### 2.4 (실습) create - react - app



    

## 2023.03.09 2주차<br>
1교시 : 전 시간에 배웠던 git 연결 및 commit 하는 법 복습 <br>
2교시 : github 아이디를 만들고 vscode와 github와 연결 한 뒤 push를 해서 Repositories에 저장하는 방법을 배움<br>
3교시 : html과 CSS에 대해서, JavaScript의 대해서와 자바스크립트의 자료형(ex/ var, let, const), 연산자(ex/ 대입, 산술, 관계, 비교, 동등, 일치, 이진 논리, 조건부, 삼항), 함수에 대해서 배웠다.
<br><br>





