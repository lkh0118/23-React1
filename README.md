# 202030223 이강현
학교 React1 과목 공부한 내용들
<br><br>

## 2023.06.01 14주차 <br>
1. 1교시
> * ### 15.1 CSS
>   * 6) 많이 사용하는 기타 속성
>   * 엘리먼트의 배경색을 지정하기 위한 background-color속성이 있다.
>   * 값으로 색상의 값이 들어가게 되는데 CSS에서 색상 값으로 사용할 수 있는 것과 예제는 아래에 있다.
>       * 16진수 컬러 값 : #ff0000
>       * 투명도를 가진 16진수 컬러값 : #ff000055
>       * RGB 컬러 값 : rgb(255, 0, 0)
>       * RGBA 컬러 값 : rgba(255, 0, 0, 0.5)
>       * HSL 컬러 값 : hsl(120, 100%, 25%)
>       * HSLA 컬러값 : hsla(120, 100%, 25%, 0.3)
>       * 미리 정의된 색상의 이름 : red
>   * 보통은 미리 정의된 색상의 이름을 사용하거나 16진수 컬러 값을 사용한다.
>   * 엘리먼트의 배경색을 지정하기 위해서는 background-color 속성의 값으로 컬러 값을 넣어주면 된다.
>   * border 속성은 border-width, border-style, border-color 등 세가지 속성을 축약시켜서 한 번에 사용할 수 있게 만든 것이다.
>   * 각 속성을 사용하여 테두리의 두께, 스타일, 색상을 지정할 수 있고, border 속성을 사용하여 한번에 지정할 수 있다.
>   * backgroudn-color 속성과 border 속성의 사용법은 아래와 같다.
```jsx
div {
    background-color: color | transparent;
    border: border-width border-style border-color
}
```
> * ### 15.2 styled-components
>   * 1) styled-componenets 설치하기
>   * npm을 사용하는 경우 (npm install --save style-components)
>   * 2) styled-components 기본 사용법
>   * 태그드 템플릿 리터럴을 사용하여 구성 요소의 스타일을 지정한다.
2. 2교시
> * 
>   * 프로그래밍에서 리터럴은 소스코드의 고정된 값을 의미한다.
>   * 템플릿 리터럴은 리터럴을 템플릿 형태로 사용하는 자바스크립트의 문법이다.
>   * backticks(`)를 사용하여 문자열을 작성하고 그 안에 대체 가능한 expression을 넣는 방법이다.
>   * 언태그드 템플릿 리터럴은 보통 문자열을 여러 줄에 걸쳐서 작성하거나 포매팅을 하기 위해서 사용한다.
>   * 태그드 템플릿 리터럴은 앞에 나와있는 태그 함수를 호출하여 결과를 리턴한다.
>   * 여기서 태그 함수의 파라미터는 expression으로 구분된 문자열 배열과 expression이 순서대로 들어가게 된다.
>   * 태그드 템플릿 리터럴을 사용하면 무자열과 expression을 태그 함수의 파라미터로 넣어 호출한 결과를 받는다.
>   * styled-components는 태그드 템플릿 리터럴을 사용하여 CSS속성이 적용된 리액트 컴포넌트를 만들어준다. 
>   * 3) styled-components의 props 사용하기
>   * Sample.jsx 작성함
3. 3교시
> * 
>   * 4) styled-components의 스타일 확장하기
>   * Sample.jsx 작성함
> * ### 15.3 (실습) styled-components를 사용하여 스타일링 해보기
>   * Blocks.jsx 작성함
> * ### 16.1 미니 블로그 기획하기
>   * 필요한 기능
>       * 글 목록 보기 기능(리스트 형태)
>       * 글 보기 기능
>       * 댓글 보기 기능
>       * 글 작성 기능
>       * 댓글 작성 기능
>   * UI는 453p 참조


## 2023.05.25 13주차<br>
1. 1교시
> * ### 14.5 여러 개의 컨텍스트 사용하기
>   * 여러 개의 컨텍스트를 동시에 사용하려면 Context Provider를 중첩해서 사용한다.
>   * 예제 코드 393p ~ 394p
>   * 예제에서는 ThemeContext와 UserContext를 중첩해서 사용하고 있다.
>   * 이러한 방법으로 여러 개의 컨텍스트를 동시에 사용 할 수 있다.
>   * 하지만 두 개 또는 그 이상의 컨텍스트 값이 자주 함께 사용될 경우 모든 값을 한번에 제공해 주는 별도의 render porp 컴포넌트를 직접 만드는 것을 고려하는 것이 좋다.
> * ### 14.6 useContext
>   * 함수형 컴포넌트에서 컨텍스트를 사용하기 위해 컴포넌트를 매번 Consumer 컴포넌트로 감싸주는 것보다 더 좋은 방법이 있다. 바로 7장에서 배운 Hook이다.
>   * useContext() 혹은 React.createContext() 함수 호출로 생성된 컨텍스트 객체를 인자로 받아서 현재 컨텍스트의 값을 리턴한다.
>   * 이 방법도 가장 가까운 상위 Provider로 부터 컨텍스트의 값을 받아온다.
>   * 만일 값이 변경되면 useContext() 훅을 사용하는 컴포넌트가 재 렌더링 된다.
>   * 또한 useContext() 훅을 사용할 때에는 파라미터로 컨텍스트 객체를 넣어줘야 한다는 것을 기억해야한다.
```jsx
function MyComponent(props) {
    const value = useContext(MyContext);

    return(
        ...
    )
}
```
> * ### 14.7 (실습) 컨텍스트를 사용하여 테마 변경 기능 만들기
2. 2교시
> * ### 15.1 CSS
>   * #### 1) CSS란
>   * CSS란 Cascading Style Sheets의 약자로써 스타일링을 위한 일종의 언어다.
>   * CSS에는 여러 가지 스타일이 정의되어 있는데 한 번에 여러 스타일이 적용될 경우에 생기는 스타일 충돌을 막기 위해 계단식으로 스타일이 적용되는 규칙을 가지고 있다.
>   * 엘리먼트에 스타일이 적용되는 규칙을 selector라고 부른다.
>   * 스타일을 어떤 엘리먼트에 적용할지 선택하게 해주는 것이다.
>   * #### 2) CSS 문법과 선택자
>   * CSS는 선택자를 먼저 쓰고 이후에 적용할 스타일을 중괄호 안에 세미콜론으로 구분하여 하나씩 기술한다.
>   * 선택자에는 해당 스타일이 적용될 HTML엘리먼트를 넣게 된다.
>   * 선택한 다음에는 중괄호 안에 적용할 스타일을 선언하고, CSS 속성의 이름과 값을 콜론으로 구분한다.
>   * 중괄호로 묶여 있는 하나의 스타일 블록에는 스타일이 여러개 들어갈 수 있다.
>   * 각 스타일은 세미콜론으로 구분한다.
>   * 선택자 사용 유형은 엘리먼트 선택자 유형과 id 선택자 유형, 클래스 선택자 유형, 전체 선택자 유형, 그룹 선택자 유형, 엘리먼트의 상태와 관련된 선택자 유형으로 총 6가지 유형이 있다.
>   * 엘리먼트 선택자 유형은 단순하게 특정 HTML태그의 이름을 써주면 된다.
>   * 두 번째로 id 선택자 유형은 HTML에서는 엘리먼트에 id를 정의할 수 있는데 이 id를 기반으로 선택하는 형태다.
>   * #뒤에 아이디를 넣어 사용한다.
>   * id 선택자는 jsx에서는 잘 사용하지 않는다.
>   * 세 번째로 클래스 선택자는 .뒤에 클래스 명을 넣어서 사용한다.
3. 3교시
>   * 네 번째로 전체 선택자 유형은 의미 그대로 특정 엘리먼트에만 선택적으로 적용하는 것이 아니라 전체 엘리먼트에 적용하기 위한 선택자이며 한국에서는 흔히 별표라고 부르는 Asterisk를 사용한다.
>   * 다섯 번째로 그룹 선택자 유형은 말 그대로 여러 가지 선택자를 그룹으로 묶어 하나의 스타일을 적용하기 위해 사용하는 선택자다.
>   * #### 3) 레이아웃과 관련된 속성
>   * 레이아웃은 정해진 공간에 가구나 물건 등을 배치하는 일을 말한다.
>   * 웹사이트에서도 비슷한 맥락으로 사용되는데 화면에 엘리먼트들을 어떻게 배치 할 것인지를 의미한다.
>   * 가장 중요한 속성은 display이다.
>   * display 속성의 값으로는 굉장히 많은 종류가 있는데 416p를 참고하자.
>   * 다음으로는 visibility이다. 가시성이라는 뜻을 가지고 있고 CSS에서는 엘리먼트를 화면에 보여주거나 감추기 위해 사용하는 속성이다.
>   * 대표적으로 visible과 hidden을 많이 사용한다.
>   * 다음은 position이다. position 속성은 엘리먼트를 어떻게 위치시킬 것인지 정의하기 위해 사용한다.
>   * #### 4) 플렉스박스
>   * 플렉스박스는 크게 컨테이너와 아이템으로 구성된다.
>   * 플렉스 컨테이너는 내부에 여러개의 엘리먼트를 포함할 수 있다.
>   * 이때 컨테이너에 포함되는 엘리먼트들이 바로 플렉스박스의 아이템이다.




## 2023.05.18 12주차<br>
1. 1교시
> * 13.1 합성에 대해 알아보기
>   * 합성은 '여러개의 컴포넌트를 합쳐서 새로운 컴포넌트를 만드는 것'이다.
>   * 조합 방법에 따라 합성의 사용 기법은 다음과 같이 나눌 수 있다.

### [1] Containment (담다, 포함하다, 격리하다)
>   * 특정 컴포넌트가 하위 컴포넌트를 포함하는 형태의 합성 방법이다.
>   * 컴포넌트에 따라서는 어떤 자식 엘리먼트가 들어올 지 미리 예상할 수 없는 경우가 있다.
>   * 특히 범용적인 '박스'역할을 하는 sidebar 혹은 Dialog와 같은 컴포넌트에서 자주 볼 수 있다.
>   * 이런 컴포넌트에서는 children prop을 사용해서 자식 엘리먼트를 출력에 그대로 전달하는 것이 좋다.
>   * 이때 children prop은 컴포넌트의 props에 기본적으로 들어있는 children 속성을 사용한다.
>   * children은 다음 구조에서 세 번째 들어가는 파라미터다.
>   * 파라미터가 배열로 되어있는 이유는 여러 개의 하위 컴포넌트를 가질 수 있기 때문이다.
>   * childre이 배열로 되어있는 것은 여러 개의 하위 컴포넌트를 위한 것이다.
>   * WelconDialog 컴포넌트는 FancyBorder 컴포넌트를 사용하고, FacnyBorder 컴포넌트는 `<h1>`과 `<p>` 두개의 태그를 children이 proops로 전달된다.
>   * 리액트에서는 props.children을 통해 하위 컴포넌트를 하나로 모아서 제공해준다.
>   * 만일 여러 개의 children 집합이 필요할 경우는 별도로 props를 정의해서 각각 원하는 컴포넌트를 넣어준다.
>   * 예와 같이 SplitPane은 화면을 왼쪽과 오른쪽으로 분할해 주고, App에서는 SplitPane을 사용해서 left, right 두 개의 props를 정의하고 있다.
>   * 즉, App에서 left, right를 props를 받아서 화면을 분할하게 된다. 이처럼 여러 개의 children 집합이 필요한 경우 별도의 props를 정의해서 사용한다.

### [2] Specialization (특수화, 전문화)
>   * 웰컴다이얼로그는 다이얼로그의 특별한 케이스다.
>   * 범용적인 개념을 구별이 되게 구체화하는 것을 특수화라고 한다.
>   * 객체지향 언어에서는 상속을 사용하여 특수화를 구현한다.
>   * 리액트에서는 합성을 사용하여 특수화를 구현한다.

### [3] Containment와 Specialization을 같이 사용하기.
>   * Containment를 위해서 props.children을 사용하고, Specialization을 위해 직접 정의한 props를 사용하면 된다. (366p 코드 참조)
>   * Dialog 컴포넌트는 이전의 것과 비슷한데 Containment를 위해 끝부분에 props.children을 추가했다.
-------------------------------------------------------------------
> * ### 13.2 상속에 대해 알아보기
>   * 합성과 대비되는 개념으로 상속(inheritance)이 있다.
>   * 자식 클래스는 부모 클래스가 가진 변수나 함수 등의 속성을 모두 갖게 되는 개념이다.
>   * 하지만 리액트에서는 상속보다는 합성을 통해 새로운 컴포넌트를 생성한다.
>   * 복잡한 컴포넌트를 쪼개 여러개의 컴포넌트로 만들고, 만든 컴포넌트를 조합하여 새로운 컴포넌트를 만든다.
2. 2교시
> * ### 13.3 (실습) Card 컴포넌트 만들기
> * ### 14.1 컨텍스트란 무엇인가
>   * 기존의 일반적인 리액트에서는 데이터가 컴포넌트의 props를 통해 부모에서 자식으로 단방향으로 전달되었다.
>   * 컨텍스트는 리액트 컴포넌트들 사이에서 데이터를 기존의 props를 통해 전달하는 방식 대신 '컴포넌트 트리를 통해 곧바로 컴포넌트에 전달하는 새로운 방식'을 제공한다.
>   * 이 것을 통해 어떤 컴포넌트라도 쉽게 데이터에 접근 할 수 있다.
>   * 컨텍스트를 사용하면 일일이 props로 전달할 필요 없이 그림처럼 데이터를 필요로 하는 컴포넌트에 곧바로 데이터를 전달 할 수 있다. (그림은 380 ~ 381p 참조)
> * ### 14.2 언제 컨텍스트를 사용해야 할까?
>   * 여러 컴포넌트에서 자주 필요로 하는 데이터는 로그인 여부, 로그인 정보, UI테마, 현재 선택된 언어 등이 있다.
>   * 이런 데이터들을 기존의 방식대로 컴포넌트의 props를 토앻 넘겨주는 예를 382p에서 보여주고 있다.
>   * 예제에서처럼 props를 통해 데이터를 전달하는 기존 방식은 실제 데이터를 필요로 하는 컴포넌트까지의 깊이가 깊어질 수록 복잡해진다.
>   * 또한 반복적인 코드를 계속해서 작성해 주어야 하기 때문에 비효율적이고 가독성이 떨어진다.
>   * 컨텍스트를 사용하면 이러한 방식을 깔끔하게 개선이 가능하다.
>   * 383p의 예제는 컨텍스트를 사용한 예다.
>   * React.createContext()함수를 사용해서 ThemeContext라는 이름의 컨텍스트를 생성한다.
>   * 컨텍스트를 사용하려면 컴포넌트의 상위 컴포넌트에서 Provider로 감싸주어야한다.
3. 3교시

>   * 예제에서는 최상위 컴포넌트읜 App 컴포넌트에서 Toolbar를 ThemeContext.Probider로 감싸주었습니다.
>   * 이렇게 하면 provider로 감싼 하위 컴포넌트가 얼마나 깊이 위치해 있는지 관계없이 컨텍스트의 데이터를 읽을 수 있다.
> * ### 14.3 컨텍스트를 사용하기 전에 고려해야 할 점
>   * 컨텍스트는 다른 레벨의 많은 컴포넌트가 특정 데이터를 필요로 하는 경우에 주로 사용된다
>   * 하지만 무조건 컨텍스트를 사용하는 것이 좋은 것은 아니다.
>   * 왜냐하면 컴포넌트와 컨텍스트가 연동되면 재사용성이 떨어지기 때문이다.
>   * 따라서 다른 레벨의 많은 컴포넌트가 데이터를 필요로 하는 경우가 아니면 props를 통해 데이터를 전달하는 컴포넌트 합성 방법이 더 적당하다.
>   * 385p의 예제처럼 실제 user와 avatarSize를 사용하는 것은 Avatar 컴포넌트 뿐인데 여러 단계에 걸쳐 props를 전달하고 있다.
>   * 이런 경우 컨텍스트를 사용하지 않고 문제를 해결할 수 있는 방법은 Avatar 컴포넌트를 변수에 저장하여 직접 넘겨주는 것이다.(9장 참고)
>   * 이렇게 하면 중간 단계의 컴포넌트들은 user와 avatarSize에 대해 몰라도 된다.
>   * 386p의 예제를 참고
>   * 하지만 386p의 예제가 모든 상황에서 좋은 것은 아니다.
>   * 데이터가 많아질수록 상위 컴포넌트가 점점 더 복잡해지기 때문이다.
>   * 이런 경우 하위 컴포넌트를 여러 개의 변수로 나누고 전달하면 된다.
>   * 387p의 예제를 참고
>   * 하위 컴포넌트의 의존성을 상위 컴포넌트와 분리 할 필요가 있는 대부분의 경우에 적합한 방법이다.
>   * 하지만 어떤 경우에는 하나의 데이터에 다양한 레벨에 있는 중첩된 컴포넌트들이 접근이 필요할 수 있다.
>   * 이러한 경우 위 방식은 사용 할 수 없고 컨텍스트를 사용해야한다.
> * ### 14.4 컨텍스트 API
>   * 이 절에서는 리액트에서 제공하는 컨텍스트 API를 통해 컨텍스트를 어떻게 사용하는지에 대해 알아보자.
>   * [1]React.createContext
>       * 컨텍스트를 생성하기 위한 함수다.
>       * 파라메타에는 기본 값을 넣어주면 된다.
>       * 하위 컴포넌트는 가장 가까운 상위 레벨의 Provider로 부터 컨텍스트를 받게 되지만, 만일 Provider를 찾을 수 없다면 위에서 설정한 기본값을 사용하게 된다.
```jsx
const MyContext = React.createContext(기본값);
```
>   * [2] Context.Provider
>       * Context.Provider 컴포넌트로 하위 컴포넌트들을 감싸주면 모든 하위 컴포넌트들이 해당 컨텍스트의 데이터에 접근 할 수 있게 된다.
```jsx
<MyContext.Provider value={/* some value */}>
```
>   * Provider 컴포넌트에는 value라는 prop이 있고, 이것은 Provider 컴포넌트 하위에 있는 컴포넌트들에게 전달된다.
>   * 그리고 하위 컴포넌트들이 이 값을 사용하게 되는데 하위 컴포넌트가 데이터를 소비한다는 의미를 가지고 있어 consumer 컴포넌트 라고 부란다.
>   * [3] Class.contextType
>       * provider 하위에 있는 클래스 컴포넌트에서 컨텍스트의 데이터에 접근하기 위해 사용된다.
>   * [4] Context.Consumer
>       * 함수형 컴포넌트에서 Context.Consumer를 사용하여 컨텍스트를 구독할 수 있다.
>       * 컴포넌트의 자식으로 함수가 올 수 있는데 이 것을 function as a child라고 부른다.
>       * Context.Consumer로 감싸주면 자식으로 들어간 함수가 현재 컨텍스트의 value를 받아서 리액트 노드로 리턴한다.
>       * 함수로 전달되는 value는 provider의 value prop과 동일하다.
```jsx
<MyContext.Consumer>
    {value => /* 컨텍스트의 값에 따라서 컴포넌트들을 렌더링 */}
</MyContext.Consumer>
```
>   * [5] Context.displayName
>       * 컨텍스트 객체는 displayName이라는 문자열 속성을 갖는다.
>       * 크롬의 리액트 개발자 도구에서는 컨텍스트의 Provider나 Consumer를 표시할때 displayName을 함께 표시해 준다.

## 2023.05.11 11주차<br>
1. 1교시
> * 중간고사 시험 점수 체크
2. 2교시
> * ### 12.1 Shared State
>   * shared state는 말 그대로 공유된 state를 의미한다.
>   * shared state는 어떤 컴포넌트의 state에 있는 데이터를 여러개의 하위 컴포넌트에서 공통적으로 사용하는 경우를 말한다.
>   * 하위 컴포넌트가 공통된 부모 컴포넌트의 state를 공유하여 사용한다.
> * ### 12.2 하위 컴포넌트에서 state 공유하기
>   * 밑은 섭씨 온도 값을 props로 받아서 물이 끓는지 안끓는지를 문자열로 출력해주는 컴포넌트다.
```jsx
function Boilingverdict(props) {
    if(props.celsius >= 100) {
        return <p>물이 끓습니다</p>;
    }
    return <p>물이 끓지 않습니다</p>;
}
```
>   * 위 코드는 BoilingVerdict라는 이름을 가진 간단한 컴포넌트다.
>   * 섭씨 온도 값을 props로 받아서 100도 이상이면 물이 끓는다 라는 문자열을 출력하고, 그 외에는 물이 끓지 않는다는 문자열을 출력한다.
>   * 아래는 이 컴포넌트를 실제로 사용하는 부모 컴포넌트다.
```jsx
function Calculator(props) {
    const [temperature, setTemperature] = useState('');

    const handleChange = (event) => {
        setTemperature(event.target.value);
    }

    return (
        <fieldset>
            <legend>섭씨 온도를 입력하세요 : </legend>
            <input
                value={temperature}
                onChange={handleChange} />
            <boilingVerdict
                celsius={paresFloat(temperature)} />
        </fieldset>
    )
}
```
>   * 사용자가 온도 값을 변경할 때마다 handleChange() 함수가 호출되고, setTemperature()함수를 통해 온도 값을 갖고있는 temperature라는 이름의 state를 업데이트한다.
>   * 다음은 Calculator 컴포넌트 안에 온도를 입력하는 컴포넌트를 추출한다
```jsx
const scaleNames = {
    c: '섭씨',
    f: '화씨'
};

function TemperatureInput(props) {
    const [temperature, setTemperature] = useState('');

    cnst handleChange = (event) => {
        setTemperature(event.target.value);
    }

    return (
        <fieldset>
            <legend>온도를 입력해주세요 (단위:{scaleNames[props.scale]}):</legend>
            <input value={temperature} onChange={handleChange} />
        </fieldset>
    )
}
```
>   * 위의 코드는 Calculator 컴포넌트에서 온도를 입력받는 부분을 추출하여 별도의 컴포넌트로 만든 것이다.
>   * 아래는 props에 단위를 나타내는 scale을 추가하여 온도의 단우를 섭씨 또는 화씨로 입력 가능 하도록 만들었다.
```jsx
function Calculator(props) {
    return(
        <div>
            <TemperatureInput scale="c" />
            <TemperatureInput scale="f" />
        </div>
    );
}
```
>   * 다음은 섭씨 온도와 화씨 온도 값을 동기화시키기 위해서 각각 변환하는 함수를 작성할 것이다.
```jsx
function toCelsius(fahrenheit) {
    return (fahrenheit - 32) * 5 / 9;
}

function toFahrenheit(celsius) {
    return (celsius * 9 / 5) + 32;
}
```
>   * 밑은 위의 함수를 호출하는 함수다.
```jsx
function tryConvert(temperature, convert) {
    const input = parseFloat(temperature);
    if(Number.isNaN(input)) {
        return'';
    }
    const output = convert(input);
    const rounded = Math.round(output * 1000) / 1000;
    return rounded.toString();
}
```
>   * tryConvert() 함수는 온도 값과 변환하는 함수를 파라미터로 받아서 값을 변환시켜 린턴해 주는 함수다.
>   * 숫자가 아닌 값을 입력하면 empty string을 리턴하도록 예외처리를 했다.
>   * 다음으로 하위컴포넌트의 state를 공통된 부모 컴포넌트로 올려서 shared state를 적용해야하는데 state를 상위 컴포넌트로 올린다는 것을 State 끌어올리기 라고 표현한다.
>   * 밑 코드는 TemperatureInput 컴포넌트에서 온도 값을 가져오는 부분을 수정한 것이다.
```jsx
return (
   //변경 전 : <input value={temperature} onChange={handleChange} />
   <input value={props.temperature} onChange={handleChange} /> 
)
```
>   * 이렇게 바꾸게 된다면 컴포넌트의 state를 사용하지 않게 되기 때문에 입력값이 변경되었을 때 상위 컴포넌트로 변경된 값을 전달해 주여야 한다.
```jsx
const handleChange = (event) => {
    const handleChange = (event) => {
        props.onTemperatureChange(event.target.value);
    }

    return (
        <fieldset>
            <legend>온도를 입력해 주세요(단위:{scaleNames[props.scale]}): </legend>
            <input value={props.temperature} onChange={handleChange} />
        </fieldset>
    )
}
```
>   * 마지막으로 변경된 TemperatureInput 컴포넌트에 맟춰서 Calculator 컴포넌트를 변경해야한다.
```jsx
function Calculator(props) {
    const [temperature, setTemperature] = userState('');
    const [scale, setScale] = useState('c');

    const handleCelsiusChange = (temperature) => {
        setTemperature(temperature);
        setScale('c');
    }

    const handleFahrenheitChang = (temperature) => {
        setTemperature(temperature);
        setScale('f');
    }

    const celsius = scale === 'f' ? tryConvert(temperature, toCelsius) : temperature;
    const fahrenheit = scale === 'c' ? tryConvert(temperature, toFahrenheit) : temperature;

    return (
        <div>
            <TemperatureInput
                scale="c"
                temperature={celsius}
                onTemperatureChange={handleCelsiusChange} />
            <TemperatureInput
                scale="f"
                temperature={fahrenheit}
                onTemperatureChange={handleFahrenheitChang} />
            <boilingVerdict
                celsius={parseFloat(celsius)} />
        </div>
    );
}
```
>   * 상위 컴포넌트인 Calculator에서 온도 값과 단위를 각각의 state로 가지고 있으며, 두 개의 하위 컴포넌트는 각각 섭씨와 화씨로 변환된 온도 값과 단위 그리고 온도를 업데이트 하기 위한 함수를 props로 갖고 있다.
>   * 이처럼 공통된 상위 컴포넌트로 올려서 공유하는 방법을 사용하면 더욱 간결하고 효율적인 개발이 가능하다.
3. 3교시
> * ### (실습) 12.3 섭씨온도와 화씨온도 표시하기


## 2023.05.04 10주차<br>
1. 1교시
> * ### 10.1 리스트와 키란 무엇인가?
>   * 라스트는 자바스크립트의 변수나 객체를 하나의 변수로 묶어 놓은 배열과 같은 것이다.
>   * 키는 각 객체나 아이템을 구분할 수 있는 고유한 값을 의미한다.
>   * 리액트에서는 배열과 키를 사용하는 반복되는 다수의 엘리먼트를 쉽게 렌더링 할 수 있다.
> * ### 10.2 여러 개의 컴포넌트 렌더링하기
>   * 예의 에어비엔비의 화면처럼 같은 컴포넌트를 화면에 반복적으로 나타내야 할 경우 배열에 들어있는 엘리먼트를 map()함수를 이용하여 렌더링한다.
>   * 다음은 numbers 배열에 들어있는 각각의 요소를 map()를 이용해서 하나씩 추출하여, 2를 곱한 후 doubled라는 배열에 다시 넣는 코드다.
```jsx
const doubled = numbers map((number) => number * 2);
```
>   * 다음은 리액트에서 map()함수를 사용한 예제다.
```jsx
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) => 
    <li>{number}</li>
);
```
>   * 이 코드는 numbers의 요소에 2를 곱하는 대신 `<li>` 태그를 결합해서 리턴하고 있다.
>   * 리턴된 listItems는 `<ul>`태그와 결합하여 랜더링 된다.
```jsx
ReactDOM.render(
    <ul>
        <li>{1}</li>
        <li>{2}</li>
        <li>{3}</li>
        <li>{4}</li>
        <li>{5}</li>
    </ul>
    document.getElementById('root')
);
```
> * ### 10.3 기본적인 리스트 컴포넌트
>   * 앞서 작성한 코드를 별도의 컴포넌트로 분리하면 다음과 같다.
>   * 이 컴포넌트는 props로 받은 숫자를 numbers로 받아 리스트로 렌더링 해준다.
```jsx
function NumberLIst(props) {
    const { numbers } = props;

    const listItems = numbers.map((number) =>
        <li>{number}</li>
    );

    return (
        <ul>{listItems}</ul>
    );
}

const numbers = [1, 2, 3, 4, 5];
ReactDOM.renter(
    <NumberList numbers={numbers} />,
    document.getElementById('root')
);
```
>   * 이 코드를 실행하면 "리스트 아이템에 무조건 키가 있어야 한다" 는 경고 문구가 나온다.
>   * 경고 문구가 나오는 이유는 각각의 아이템에 key props가 없기 때문이다.
> * ### 10.4 리스트의 키에 대해 알아보기
>   * 리스트에서의 키는 "리스트에서 아이템을 구별하기 위한 고유한 문자열" 이다.
>   * 이 키는 리스트에서 어떤 아이템이 변경, 추가 또는 제거되었는지 구분하기 위해서 사용한다.
>   * 키는 같은 리스트에 있는 엘리언트 사이에서만 고유한 값이면 된다.
> * ### 10.5 (실습) 출석부 출력하기
2. 2교시

> * ### 11.1 폼이란 무엇인가?
>   * 폼은 일반적으로 사용자로부터 입력을 받이 귀한 양식에서 많이 사용된다.
> * ### 11.2 제어 컴포넌트
>   * 제어 컴포넌트는 사용자가 입력한 값에 접근하고 제어할 수 있도록 해주는 컴포넌트다.
>   * 다음 코드는 사용자의 이름을 입력 받는 HTML폼을 리액트 제어 컴포넌트로 만든 것이다.
```jsx
function NameForm(props) {
    const [value, setValue] = useState('');

    const handleChange = (event) => {
        setValue(event.target.value);
    }

    const handleSubmit = (event) => {
        alert('입력한 이름: ' + value);
        event.preventDefault();
    }

    return (
        <form onSubmit={handleSubmit}>
            <label>
                이름:
                <input type="text" value={value} onChange={handleChange} />
            </label>
            <button type="submit">제출</button>
        </form>
    )
}
```
> * ### 11.3 textarea 태그
>   * HTML에서는 `<textarea>`태그의 children으로 텍스트가 들어가는 형태다.
>   * 리액트에서는 state를 통해 `<textarea>` 태그에 value라는 attribute를 사용하여 텍스트를 표시한다.
> * ### 11.4 select 태그
>   * select 태그도 textarea와 동일하다.
```html
<select>
    <option value="apple">사과</option>
    <option value="banana">바나나</option>
    <option selected value="grape">포도</option>
    <option value="watermelon">오렌지</option>
</select>
```
```jsx
function FruitSelect(props) {
    const [value, setValue] = useState('grape');

    const handleChange = (event) => {
        setValue(event.target.value);
    }

    const handleSubmit = (event => {
        alert('선택한 과일: ' + value);
        event.preventDefault();
    })

    return(
        <from onSubmit={handleSubmit}>
            <label>
                과일을 선택하세요:
                <select value={value} onChange={handleChange}>
                    <option value="apple">사과</option>
                    <option value="banana">바나나</option>
                    <option value="grape">포도</option>
                    <option value="watermelon">수박</option>
                </select>
            </label>
            <button type="submit">제출</button>
        </form>
    )
}
```
3. 3교시
> * ### 11.5 File input 태그
>   * File input 태그는 그 값이 읽기 전용이기 때문에 리액트에서는 비제어 컴포넌트가 된다.
> * ### 11.7 Input Null Value
>   * 제어 컴포넌트에 value prop을 정해진 값으로 넣으면 코드를 수정하지 않는 한 입력값을 바꿀 수 없다.
>   * 만약 value prop은 넣되 자유롭게 입력 할 수 있게 만들고 싶다면 값이 undefined 또는 null값을 넣어주면 된다.
```jsx
ReactDom.render(<input value="hi" />, rootNode);

setTimeout(function() {
    ReactDom.render(<input value={null} />, rootNode);
}, 1000);
```
> * ### 11.8 (실습) 사용자 정보 입력받기

## 2023.04.27 9주차<br>

1. 1교시
> * ### 8.1 이벤트 처리하기
>   * DOM에서 클릭 이벤트를 처리하는 예제 코드
```javascript
<button onclick="activate()">
    Activate
</button>
```
>   * React에서 클릭 이벤트 처리하는 예제 코드
```javascript
<button onClick={activate}>
    Activate
</button>
```
>   * 둘의 차이점은
>   1) 이벤트 이름이 onclick에서 onClick으로 변경.(Camel case)
>   2) 전달하려는 함수는 문자열에서 함수 그대로 전달.
>   * 이벤트가 발생했을 때 해당 이벤트를 처리하는 함수를 "이벤트 핸들러(Event Handler)" 라고 한다. 또는 이벤트가 발생하는 것을 계속 듣고 있다는 의미로 "이벤트 리스너(Event Listener)"라고 한다.
>   * 이벤트 핸들러 추가하는 방법은
>   * 버튼을 클릭하면 이벤트 핸들러 함수인 handleClick() 함수를 호출하도록 되어있다.
>   * bind를 사용하지 않으면 this.handleClick은 글로벌 스코프에서 호출되어, undefined으로 사용할 수 없기 때문이다.
>   * bind를 사용하지 않으려면 화살표 함수를 사용하는 방법도 있다.
>   * 하지만 클래스 컴포넌트는 이제 사용하지 않기 때문에 이 내용은 참고만 하자.
```javascript
class Toggle extends React.Component {
    constructor(props) {
        super(props);

        this.state = {isToggleOn: true };

        this.handleClick = this.handleClick.bind(this);
    }

    handleClick() {
        this.setState(prevState => ({
            isToggleOn: !prevState.isToggleOn
        }));
    }

    render() {
        return (
            <button onClick={this.handleClick}>
                {this.statie.isToggleOn ? '켜짐' : '꺼짐'}
            </button>
        )
    }
}
```
>   * 클래스형을 함수형으로 바꾸면 다음 코드와 같다.
>   * 함수형에서 이벤트 핸들러를 정의하는 방법은 두가지다.
>   * 함수형에서는 this를 사용하지 않고, onClick에서 바로 HandleClick을 넘기면 된다.
```javascript
function Toggle(props) {
    const [isToggleOn, setIsToggleOn] = useState(true);

    //방법 1. 함수 안에 함수로 정의
    function handleClick() {
        setIsToggleOn((isToggleOn) => !isToggleOn);
    }

    //방법 2. arrow function을 사용하여 정의
    const handleClick = () => {
        setIsToggleOn((isToggleOn) => !isToggleOn);
    }

    return (
        <button onClick={handleClick}>
            {isToggleOn ? "켜짐" : "꺼짐" }
        </button>
    );
}
```
> * ### 8.2 Arguments 전달하기
>   * 함수를 정의할 때는 피라미터(parameter) 혹은 매개변수, 함수를 사용할 때는 아귀먼트(Argument) 혹은 인자라고 부른다.
>   * 이벤트 핸들러에 매개변수를 전달해야 하는 경우도 많습니다.
```javascript
<button onClick={(event) => this.deleteItem(id, event)}>삭제하기</button>
<button onClick={this.deleteItem.bind(this, id)}>삭제하기</button>
```
>   * 위의 코드는 모두 동일한 역할을 하지만 하나는 화살표 함수를, 다른 하나는 bind를 사용했다.
>   * event라는 매개변수는 리액트의 이벤트 객체를 의미한다.
>   * 두 방법 모두 첫 번째 매개변수는 id이고 두 번째 매개변수로 event가 전달된다.
>   * 첫 번째 코드는 명시적으로 event를 매개변수로 넣어 주었고, 두 번째 코드는 id 이후 두번째 매개변수로 event가 자동 전달 된다. (이 방법은 클래스형에서 사용하는 방법이다.)
>   * 함수형 컴포넌트에서 이벤트 핸들러에 매개변수를 전달할 때는 254페이지 코드와 같이 한다.

2. 2교시
> * ### 8.3 (실습) 클릭 이벤트 처리하기
>   1) ConfirmButton 컴포넌트 만들기.
>   2) 클래스 필드 문법 사용하기
>   3) 함수 컴포넌트로 변경하기
> * ### 9.1 조건부 렌더링이란?
>   * 여기서 조건이란 우리가 알고 있는 조건문의 조건이다.
```javascript
function Greeting(props) {
    const isLoggedIn = props.isLoggedIn;
    if (isLoggedIn) {
        return <UserGreeting />;
    }
    return <GuestGreeting />;
}
```
>   * props로 전달 받은 isLoggedIn이 true면 <UserGreeting />을, false면 <GuestGreeting /> 을 return한다.
>   * 이와 같은 렌더링을 조건부 렌더링이라고 한다.
> * ### 9.2 엘리먼트 변수
>   * 렌더링해야 될 컴포넌트를 변수처럼 사용하는 방법이 엘리먼트 변수다.
>   * 272페이지 코드처럼 state에 따라 button 변수에 컴포넌트의 객체를 저장하여 return문에서 사용하고 있다.
```javascript
fucntion LoginControl(props) {
    const [isLoggedIn, setIsLoggedIn] = useState(false);

    const handleLoginClick = () => {
        setIsLoggedIn(true);
    }

    const handleLogoutClick = () => {
        setIsLoggedIn(false);
    }

    let button;
    if (isLoggedIn) {
        button = <LogoutButton onClick={handleLogoutClick} />;
    } else {
        button = <LoginButton onClick={handleLoginClick} />;
    }

    return (
        <div>
            <Greeting isLoggedIn={isLoggedIn} />
            {button}
        </div>
    )
}
```
> * ### 9.3 인라인 조건
>   * 필요한 곳에 조건문을 직접 넣어 사용하는 방법이다.
>   1) 인라인 if
>   * if문을 직접 사용하지 않고, 동일한 효과를 내기 위해 && 논리 연산자를 사용한다.
>   * &&는 and연산자로 모든 조건이 참일때만 참이 된다.
>   * 첫 번째 조건이 거짓이면 두 번째 조건은 판단할 필요가 없다. 단축평가
```javascript
true && expression -> expression
false && expression -> false
```
```jsx
function Mailbox(props) {
    const unreadMessages = props.unreadMessages;

    return (
        <div>
            <h1>안녕하세요!</h1>
            {unreadMessage.length > 0 &&
                <h2>현재 {unreadMessages.length}개의 읽지 않은 메시지가 있습니다.
                </h2>
            }
        </div>
    );
}
```
>   * 판단만 하지 않는 것이고 결과 값은 그대로 리턴된다.

3. 3교시
>   2) 인라인 if - else
>   * 삼항 연산자를 사용한다.
>   * 문자열이나 엘리먼트를 넣어서 사용할 수도 있다.
```jsx
function UserState(props) {
    return (
        <div>
            이 사용자는 현재 <b>{props.isLoggedIn ? '로그인' : '로그인하지 않은'} </b> 상태 입니다.
        </div>
    )
}
```
> * ### 9.4 컴포넌트 렌더링 막기
>   * 컴포넌트를 렌더링하고 싶지 않을 때에는 null을 리턴한다.
```jsx
function WarningBanner(props) {
    if (!props.warning) {
        return null;
    }

    return (
        <div>경고!</div>
    );
}
```
> * ### 9.5 (실습) 로그인 여부를 나타내는 툴바 만들기


## 2023.04.13 7주차<br>
1. 1교시
> * ### 7.1 훅이란 무엇인가?
>   * 클래스형 컴포넌트에서는 생성자(constructor)에서 state를 정의하고, setState() 함수를 통해 state를 업데이트한다.
>   * 예전에 사용하던 함수형 컴포넌트는 별도로 state를 정의하거나, 컴포넌트의 생명주기에 맟춰서 어떤 코드가 실행되도록 할 수 없었다.
>   * 함수형 컴포넌트에서도 state나 생명주기 함수의 기능을 사용하게 해주기 위해 추가된 기능이 바로 훅(Hook)이다.
>   * 함수형 컴포넌트도 훅을 사용하여 클래스형 컴포넌트의 기능을 모두 통일하게 구현할 수 있게 되었다.
>   * Hook이란 'state와 생명주기 기능에 갈고리를 걸어 원하는 시점에 정해진 함수를 실행되도록 만든 함수'를 의미한다
>   * 훅의 이름은 모두 'use'로 시작한다.
>   * 사용자 정의 훅(custom hook)을 만들 수 있으며, 이 경우에 이름은 자유롭게 할 수있으나 'use'로 시작을 해야한다.
> * ### 7.2 useState
>   * useState는 함수형 컴포넌트에서 state를 사용하기 위한 Hook이다.
>   * 다음 예제는 버튼을 클릭 할 때마다 카운트가 증가하는 함수형 컴포넌트다.
>   * 하지만 증가는 시킬 수 있지만 증가할 때마다 재 렌더링은 일어나지 않는다.
>   * 이럴 때 state를 사용해야 하지만 함수형에는 없기 때문에 useState()를 사용한다.
```javascript
import React, { useState } from "react";

function Counter(props) {
    var count = 0;

    return(
        <div>
            <p>총 {count}번 클릭했습니다.</p>
            <button onClick={() => count++}>
                클릭
            </button>
        </div>
    )
}
```
>   * 첫번째 항목은 state의 이름(변수명)이다.
>   * 두번째 항목은 state의 set함수이다. 즉 state를 업데이트 하는 함수다.
>   * 함수를 호출 할 때 state의 초기값을 설정한다.
>   * 함수의 리턴 값은 배열의 형태다
```javascript
import React, { useState } from "react";

function Counter(props) {
    const [count, setCount] = useState(0);

    return(
        <div>
            <p>총 {count}번 클릭했습니다.</p>
            <button onClick={() => setCount(count + 1)}>
                클릭
            </button>
        </div>
    );
}
```
> * ### 7.3 useEffect
>   * useState와 함께 가장 많이 사용하는 Hook이다.
>   * 이 함수는 사이드 이펙트를 수행하기 위한 것이다.
>   * 영어로 side effect는 부작용을 의미한다. 일반적으로 프로그래밍에서 사이트 이펙트는 '개발자가 의도하지 않은 코드가 실행되면서 버그가 발생하는 것'을 말한다.
>   * 하지만 리액트에서는 효과 또는 영향을 뜻하는 effect의 의미에 가깝다.
>   * 예를 들면 서버에서 데이터를 받아오거나 수동으로 DOM을 변경하는 등의 작업을 의미한다.
>   * 이 작업을 이펙트라고 부르는 이유는 이 작업들이 다른 컴포넌트에 영향을 미칠 수 있으며, 렌더링 중에는 작업이 완료 될 수 없기 때문이다. 랜더링이 끝난 이후에 실행되어야 하는 작업들이다.
>   * 클래스 컴포넌트의 생명주기 함수와 같은 기능을 하나로 통합한 기능을 제공한다.
>   * useEffect가 side effect가 아니라 effect에 가깝다고 설명하고 있지만, 이 것은 부작용의 의미를 잘못 해석해서 생긴 오해다. 부작용의 부를 아닐 부로 생각했다.
>   * side effect는 '원래 용도 혹은 목적의 효과 외에, 부수적으로 다른 효과가 있는 것'을 뜻한다.
>   * 결국 side effect는 렌더링 외에 실행해야 하는 부수적인 코드들을 말한다.
>   * 예를 들면 네트워크 리퀘스트, DOM 수동 동작, 로킹 혹은 정리(clean - up)가 필요 없는 경우들을 말한다.
>   * useEffect()함수는 다음과 같이 사용한다.
>   * 첫번째 파라미터는 이펙트 함수가 들어가고, 두번째 파라미터는 의존성 배열이 들어간다.<br>
``` useEffect(이펙트 함수, 의존성 배열);```
>   * 의존성 배열은 이펙트가 의존하고 있는 배열로, 배열 안에 있는 변수 중에 하나라도 값이 변경되었을 때 이펙트 함수가 실핸된다.
>   * 이펙트 함수는 처음 컴포넌트가 렌더링 된 이후, 그리고 재 렌더링 이후에 실행된다.
>   * 만약 이펙트 함수가 마운트와 언마운트 될 때만 한 번씩 실행되게 하고 싶다면, 빈 배열을 넣으면 된다. 이 경우 props나 state에 있는 어떤 값에도 의존하지 않기 때문에 여러 번 실행되지 않는다.
>   * 의존성 배열을 생략하는 경우에는 업데이트 될 때마다 호출된다.
>   * 정리하면 다음과 같다.
```javascript
useEffect(() => {
    //컴포넌트가 마운트 된 이후
    //의존성 배열에 있는 변수들 중 하나라도 같이 변경 되었을 때 실행됨
    //의존성 배열에 빈 배열([])을 넣으면 마운트와 언마운트시에 단 한 번씩만 실행됨
    //의존성 배열 생략 시 컴포넌트 업데이트 시마다 실행됨

    return () => {
        //컴포넌트가 마운트 해제되기 전에 실행됨
    }
}
), [의존성 변수1, 의존성 변수2, ...]
```
> * ### 7.4 useMemo
>   * useMemo() 혹은 Memoizde value를 리턴하는 훅이다.
>   * 이전 계산 값을 갖고 있기 때문에 연산량이 많은 작업의 반복을 피할 수 있다.
>   * 이 훅은 렌더링이 일어나는 동안 실행된다.
>   * 따라서 렌더링이 일어나는 동안 실행돼서는 안될 작업을 넣으면 안된다.
>   * 예를 들면 useEffect에서 실행되어야 할 사이드 이펙트 같은 것이다.

2. 2교시
```javascript
const memoizedValue = useMemo(
    () => {
        //연산량이 높은 작업을 수행하여 결과를 반환
        return computeExpensiveValue(의존성 변수1, 의존성 변수2);
    },
    [의존성 변수1, 의존성 변수2]
)
```
>   * 다음 코드와 같이 의존성 배열을 넣지 않을 경우, 렌더링이 일어날 때마다 매번 함수가 실행된다.
>   * 따라서 의존성 배열을 넣지 않는 것은 의미가 없다.
>   * 만약 빈 배열을 넣게 되면 컴포넌트 마운트 시에만 함수가 실행된다.
```javascript
const memoizedValue = useMemo(
    () => computeExpensiveValue(a, b)
);
```
> * ### 7.5 useCallback
>   * useCallback() 훅은 useMemo()와 유사한 역할을 합니다.
>   * 차이점은 값이 아닌 함수를 반환한다는 점이다.
>   * 의존성 배열을 파라미터로 받는 것은 useMemo()와 동일하다.
>   * 파라미터로 받은 함수를 콜백이라고 부른다
>   * useMemo와 마찬가지로 의존성 배열 중 하나라도 변경되면 콜백함수를 반환한다
```javascript
const memoizedCallback = useCallback(
    () => {
        doSomething(의존성 변수1, 의존성 변수2)
    },
    [의존성 변수1, 의존성 변수2]
);
```
> * ### 7.6 useRef
>   * useRef() 훅은 레퍼런스를 사용하기 위한 훅이다.
>   * 레퍼런스란 특정 컴포넌트에 접근할 수 있는 객체를 의미한다.
>   * useRef() 훅은 바로 이 레퍼런스 객체를 반호나한다,
>   * 레퍼런스 객체에는 .current라는 속성이 있는데, 이것은 현재 참조하고 있는 엘리먼트를 의미한다.
```javascript
        const refContainer = useRef(초깃값);
```
>   * 이렇게 반환된 레퍼런스 객체는 컴포넌트의 라이프타임 전체에 걸쳐서 유지된다.
>   * 즉, 컴포넌트가 마운트 해제 전까지는 계속 유지된다는 의미다.
> * ### 7.7 훅의 규칙
>   * 첫 번째 규칙은 무조건 최상의 레벨에서만 호출해야 한다는 것이다. 여기서 최상위는 컴포넌트의 최상위 레벨을 의미한다.
>   * 따라서 반복문이나 조건문 또는 중첩된 함술들 안에서 훅을 호출하면 안된다.
>   * 이 규칙에 따라서 훅은 컴포넌트가 렌더링 될 때마다 같은 순서로 호출되어야 한다.
>   * 페이지 224의 코드는 조건에 따라 호출됨으로 잘못된 코드다.
>   * 두번째 규칙은 리액트 함수형 컴포넌트에서만 훅을 호출해야 한다는 것이다.
>   * 따라서 일반 자바스크립트 함수에서 훅을 호출하면 안된다.
>   * 훅은 리액트의 함수형 컴포넌트 혹은 직접 만든 커스텀 훅에서만 호출 할 수 있다.
> * ### 7.8 나만의 훅 만들기
>   * 필요하다면 직접 훅을 만들어 쓸 수도 있다. 이 것을 커스텀 훅이라고 한다.
> * #### 1. 커스텀 훅을 만들어야 하는 상황
>   * 예제 UserStatus 컴포넌트는 isOnline이라는 state에 따라서 사용자의 상태가 온라인인지 아닌지를 텍스트로 보여주는 컴포넌트다.
```javascript
import React, { useState, useEffect } from "react";

function UserStatus(props) {
    const [isOnline, setIsOnline] = useState(null);

    useEffect(() => {
        function handleStatusChange(status) {
            setIsOnline(status.isOnline);
        }

        ServerAPI.subscribeUserStatus(props.user.id, handleStatusChange);
        return () => {
            ServerAPI.unsubscribeUserStatus(props.user.id, handleStatusChange);
        }
    });

    if (isOnline === null) {
        return '대기중...';
    }

    return isOnline ? '온라인' : '오프라인';
}
```
> * #### 2. 커스텀 훅 추출하기
>   * 두 개의 자바스크립트 함수에서 하나의 로직을 공유하도록 하고 싶을 때 새로운 함수를 하나 만드는 방법을 사용한다.
>   * 리액트 컴포넌트와 훅은 모두 함수이기 때문에 동일한 방법을 사용 할 수 있다.
>   * 이름을 use로 시작하고, 내부에서 다른 훅을 호출하는 자바스크립트 함수를 만들면 된다.
>   * 한 가지 주의 할 점은 일반 컴포넌트와 마찬가지로 다른 훅을 호출하는 것은 무조건 커스텀 훅의 최상위 레벨에서만 해야한다.
>   * 커스텀 훅은 일반 함수와 같다고 생각해도 된다.
>   * 다만 이름은 use로 시작하도록 한다는 것만 다르다.
> * #### 3. 커스텀 훅 사용하기

3. 3교시
> * ### 7.9 (실습) 훅을 사용한 컴포넌트 개발 (chapter_07 폴더에 있는 useCounter.jsx, Accommodate.jsx 파일 참조)

## 2023.04.06 6주차<br>
1. 1교시
> * ### 5.5 컴포넌트 추출
>   * 복잡한 컴포넌트를 쪼개서 여러 개의 컴포넌트로 나눌 수도 있다.
>   * 큰 컴포넌트에서 일부를 추출해서 새로운 컴포넌트를 만드는 것이다. <br><br> p.s. 실무에서는 처음부터 1개의 컴포넌트에 하나의 기능만 사용하도록 설계하는것이 좋다.
>   * Comment는 댓글 표시 컴포넌트다.
>   * 내부에는 이미지, 이름, 댓글과 작성일이 포함되어 있다.
>   * 첫 번째로 이미지 부분을 Avater 컴포넌트로 추출
```javascript 
function Avater(props) {
    return (
        <img className = "avater"
            src = {props.user.avaterUrl}
            alt = {prop.user.name}
        />
    );
}
```
>   * 두 번째로 사용자 정보 부분을 추출
>   * 컴포넌트 이름은 UserInfo로 한다. 
>   * UserInfo 안에 Avater 컴포넌트를 넣어서 완성시키기
```javascript
function UserInfo(props) {
    return (
        <div className="user-info">
            <Avater user={props.user} />
            <div className="user-info-name">
                {props.user.name}
            </div>
        </div>
    );
}
```
>   * 추출 후 다시 결합한 UserInfo를 Comment 컴포넌트에 반영하면 다음과 같은 모습이 된다.
>   * 처음에 비해 가독성이 높아진 것을 확인 가능
```javascript
function Comment(props) {
    return (
        <div className = "comment">
            <UserInfo user={props.author} />
            <div className="comment-text">
                {props.text}
            </div>
            <div className="comment-date">
                {formatDate(props.date)}
            </div>
        </div>
    );
}
```
> * ### 5.6 (실습) 댓글 컴포넌트 만들기 (chapter_05 Comment.jsx 참조)
>   * 프로젝트 디렉토리에 /src/chapter_05 디렉토리를 새로 생성
>   * 그 안에 Comment.jsx라는 파일 생성
>   * Comment 컴포넌트 만들기
>   * 그 다음 CommentList.js를 생성, 컴포넌트를 다음과 같이 코딩
>   * CommentList를 렌더링하기 위해 index.js를 다음과 같이 수정
>   * 4장에서 사용했던 setInterval(() => {}, 1000) 부분은 삭제
>   * `<Clock />`을 `<CommentList />`로 수정.
>   * Comment 컴포넌트에 css를 다음과 같이 작성
>   * 다음으로 Comment에 style을 적용할 수 있도록 다음과 같이 수정

2. 2교시
>   * 이번에는 Comment를 범용으로 사용 할 수 있도록 이름과 코멘트를 props로 받도록 수정
>   * props로 전달받은 것이 없어서 아무 것도 출력되지 않음
>   * 이렇게 코드를 작성하면 매번 컴포넌트를 수정해야 하기 때문에 나쁜 코드의 예다.
>   * 별도의 객체로 받아 컴포넌트에서 분리하여 출력하도록 해야 한다.
>   * 이때 사용하는 함수가 map() 함수다.
> * ### 6.1 state
> * #### 1. State란?
>   * State는 리액트 컴포넌트의 상태를 의미한다.
>   * 상태의 의미는 정상인지 비정상인지가 아니라 컴포넌트의 데이터를 의미한다.
>   * 정확히는 컴포넌트의 변경가능한 데이터를 의미한다.
>   * State가 변하면 다시 렌더링이 되기 때문에 렌더링과 관련된 값만 state에 포함시켜야 한다.
> * #### 2.state의 특징
>   * 리액트 만의 특별한 형태가 아닌 단지 자바스크립트 객체일 뿐이다.
>   * 예의 LikeButton은 class 컴포넌트다.
>   * constructor는 생성자이고 그 안에 있는 this.state가 현 컴포넌트의 state다.
```javascript
class LikeButton extends React.Component {
    constructor(props) {
        super(props);

        this.state = (
            liked: false
        );
    }
}
```
>   * 함수형에서는 useState()라는 함수를 사용한다.
>   * state는 변경 가능하다고 했지만 직접 수정해서는 안된다.
>   * 불가능하다고 생각하는 것이 좋다.
>   * state를 변경하고자 할 때에는 setstate()함수를 사용한다.

3. 3교시
> * ### 6.2 생명주기에 대해 알아보기
>   * 생명주기는 컴포넌트의 생성 시점, 사용 시점, 종료 시점을 나타내는 것이다.
>   * constructor가 실행되면서 컴포넌트가 생성된다
>   * 생성 직후 componentDidMount()함수가 호출된다.
>   * 컴포넌트가 소멸하기 전까지 여러 번 렌더링 한다.
>   * 렌더링은 props, setState(), forceUpdate()에 의해 상태가 변경되면 이루어진다.
>   * 렌더링이 끝나면 commponentDinUpdate() 함수가 호출된다.
>   * 컴포넌트가 언마운트 되면 componentWillUnmount()함수가 호출된다.
> * ### 6.3 (실습) state와 생명주기 함수 사용하기 (실습은 파일 참조)
> * #### 2. (실습) React Developer Tools 설치
>   * 구글에서 'React Developer Tools'로 검색하면 찾을 수 있다.
>   * 스폰서 링크 때문에 교재처럼 맨 위에 오지 않을 수 있다.
>   * 링크를 클릭하면 'chrome 웹 스토어'로 이동된다.
>   * 'Chrome에 추가'버튼을 클릭해서 설치한다.




## 2023.03.30 5주차<br>
1. 1교시
> * ### 4.1 엘리먼트에 대해 알아보기
>   * 엘리먼트는 리액트 앱을 굿어하는 요소를 의미한다.
>   * 공식페이지에는 "엘리먼트는 리액트 앱의 가장 작은 빌딩 블록"이라고 설명
>   * 웹사이트 의 경우는 DOM 엘리먼트이며 HTML요소를 의미한다.
>   * 리액트 엘리먼트와 DOM엘리먼트의 차이점
>       * 리액트 엘리먼트는 Virtual DOM의 형태를 취하고 있다.
>       * DOM 엘리먼트는 페이지의 모든 정보를 가지고 있어 무겁다.
>       * 리액트 엘리먼트는 변화한 부분만 가지고 있어 가볍다.
> * #### 1. 엘리먼트의 생김새
>   * 리액트 엘리먼트는 자바스크립트 객체의 형태로 존재한다.
>   * 컴포넌트(Button 등), 속성(color 등) 및 내부의 모든 children을 포함하는 일반 JS객체다.
>   * 이 객체는 마음대로 변경 할 수 없는 불변성을 갖고 있다.
>   * 리액트 엘리먼트의 예를 보면 type에 태그 대신 리액트 컴포넌트가 들어가 있는 것 외에는 차이가 없다.
>   * 자바 스크립트 객체다.
>   * 내부적으로 자바 스크립트 객체를 만드는 역할을 하는 함수는 createElement()다.
>       * 첫 번째 매개변수가 type다. 이 곳에 태그가 들어가면 그대로 표현하고, 만일 리액트 컴포넌트가 들어가면 이 것을 분해해 결국 태그로 만들게 된다.
>       * 두 번째 매개변수인 props는 속성을 나타낸다
>       * 세 번째 매겨변수는 children이다.
> * #### 2. 엘리먼트의 특징
>   * 리액트 엘리먼트의 가장 큰 특징은 불변성이다
>   * 한 번 생성된 엘리먼트의 children이나 속성을 바꿀 수 없다.
>   * 만약 내용이 바뀐다면?
>       * 컴포넌트를 통해 새로운 엘리먼트를 생성해야 한다.
>       * 그 다음 이전 엘리먼트와 교체하는 방법으로 내용을 바꾸는 것
>       * 교체하는 작업을 하기 위해 Virtual DOM을 사용합니다.
> * ### 4.3 랜더링 된 엘리먼트 업데이트하기
>   * 다음 코드는 tick() 함수를 정의하고 있다.
>   * 이 함수는 현재 시간을 포함한 element를 생성하여 root div에 렌더링해 준다.
>   * 라인 12번을 보면 setInterval()함수를 이용해서 정의한 tick()을 1초에 한번씩 호출하고 있다.
>   * 결국 1초에 한번씩 element를 새로 만들고 그 것을 교체하는 것이다.
>   * 다음 코드를 실행하고 크롬 개발자도구에서 확인해 보면 시간 부분만 업데이트 되는 것을 확인 할 수 있다.

2. 2교시
> * ### 4.3 랜더링 된 엘리먼트 업데이트하기
>   * clock.html 만들기
> * ### 4.4 (실습) 시계 만들기
>   1. 이전에 만들었던 프로젝트 디렉토리를 오픈
>   2. chapter_04라는 디렉토리를 생성 
>   3. 디렉토리 안에 Clock.jsx라는 이름으로 파일을 생성
>   4. Clock 컴포넌트 만들기
>   5. 다음 index.js를 수정하여 1초에 한번씩 Clock 컴포넌트를 root div에 렌더링하도록 한다.

3. 3교시
> * ### 5.1 컴포넌트에 대해 알아보기
>   * 2장에서 설명한 바와 같이 리액트는 컴포넌트 기반의 구조를 갖는다.
>   * 컴포넌트 구조라는 것은 작은 컴포넌트가 모여 큰 컴포넌트를 구성하고, 다시 이런 컴포넌트들이 모여서 전체 페이지를 구성한다는 것을 의미한다.
>   * 컴포넌트 재사옹이 가능하기 때문에 전체 코드의 양을 줄일 수 있어 개발 시간과 유지 보수 비용도 줄일 수 있다.
>   * 컴포넌트는 자바스크립트 함수와 입력과 출력이 있다는 면에서는 유사하다.
> ### 5.2 Props에 대해 알아보기
> #### 1. Props의 개념
>   * props는 prop(property : 속성, 특성)의 준말이다.
>   * 이 props가 바로 컴포넌트의 속성이다.
>   * 컴포넌트에 어떤 속성, props를 넣느냐에 따라서 속성이 다른 엘리먼트가 출력된다.
>   * props는 컴포넌트에 전달 할 다양한 정보를 담고 있는 자바스크립트 객체다.
> #### 2. Props의 특징
>   * 읽기 전용이다. 변경 할 수 없다는 의미
>   * 속성이 다른 엘리먼트를 생성하려면 새로운 props를 컴포넌트에 전달하면 된다.
>   * Pure 함수 vs Impure 함수
>       * Pure 함수는 인수로 받은 정보가 함수 내부에서도 변하지 않는 함수
>       * Impure 함수는 인수로 받은 정보가 함수 내부에서 변하는 함수
> #### 3. Props의 사용법
>   * JSX에서는 key-value쌍으로 props를 구성한다
>   * JSX를 사용하지 않는 경우 props의 전달 방법은 createElement() 함수를 사용하는 것이다.
> * ### 5.3 컴포넌트 만들기
> * #### 1. 컴포넌트의 종류
>   * 리액트 초기버전을 사용할 때에는 클래스형 컴포넌트를 주로 사용했다.
>   * 이후 Hook이라는 개념이 나오면서 최근에는 함수영 컴포넌트를 주로 사용한다.
>   * 예전에 작성된 코드난 문서들이 클래스형 컴포넌트를 사용하고 있기 때문에 클래스형 컴포넌트와 컴포넌트의 생명주기에 관해서도 공부해 두어야 한다.
> * #### 2. 함수형 컴포넌트
>   * Welcome컴포넌트는 props를 받아, 받은 props중 name키의 값을 "안녕," 뒤에 넣어 반환<br><br>
        `function Welcome(props) {`<br>`
           return <h1>안녕, {props.name}</h1>;`<br>`
        }`
> * #### 3. 클래스형 컴포넌트
>   * Welcome컴포넌트는 React.Commponent class로 부터 상속을 받아 선언<br><br>
        `class Welcome extends React.Componenet {`<br>`
            render() {`<br>`
                return <h1>안녕, {this.props.name}</h1>;
            }`<br>`
        }`
> * #### 4. 컴포넌트 이름 짓기
>   * 이름은 항상 대문자로 시작
>   * 리액트는 소문자로 시작하는 컴포넌트를 DOM 태그로 인식하기 때문
>   * 컴포넌트 파일 이름과 컴포넌트 이름은 같게 설정

> * ### 5.4 컴포넌트 합성
>   * 컴포넌트 합성은 여러 개의 컴포넌트를 합쳐서 하나의 컴포넌트를 만드는 것
>   * 리액트에서는 컴포넌트 안에 또 다른 컴포넌트를 사용할 수 있기 때문에 복잡한 화면을 여러개의 컴포넌트로 나누어 구현할 수 있다.

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
> * ### 3.5 (실습) JSX 코드 작성해 보기
>   * create-react-app으로 만든 프로젝트를 VSCode로 연다.
>   * src 디렉토리에 'chapter_03'이라는 디렉토리를 생성한다.
>   * 생성한 디렉토리에 Book.jsx라는 파일을 생성한다.
>   * Book.jsx를 생성한 디렉토리에 Library.jsx 파일을 생성한다.
>   * 프로젝트 root의 index.js 파일을 오픈한다.
>   * Library컴포넌트를 import한다.
>   * render 함수에서 App을 Library 컴포넌트로 수정한다
>   * npm start로 app을 실행하고 결과를 확인한다.

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





