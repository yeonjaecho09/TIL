# React의 기초(React란?)
## React란?
  - React는 사용자 인터페이스(UI)를 만들기 위한 JavaScript 기반의 라이브러리이다.
  - React는 UI를 컴포넌트라는 단위로 나누어 관리하는 방식으로 UI를 만들고 관리할 수 있게 해준다
    - 즉, **React는 UI를 컴포넌트 단위로 나누어 구성하는 JavaScript 기반의 라이브러리** 라고 말할 수 있다

## 컴포넌트란?
  - 컴포넌트란 하나의 독립적인 UI 조각을 말한다.
  - 예시로 React에서 입력창이나 각각의 버튼들이 하나의 컴포넌트라고 말할 수 있다.
### 컴포넌트는 어떻게 만들어질까?
  - 컴포넌트는 JavaScript의 함수 형식으로 만들어진다.
  ```
  const MyComponent = () => {
    return(
      <>
        <h1>hello react!!</h1>
      </>
    )
  }
  ```
  - 이런식으로 JS함수로 정의하며 반환값 부분을 HTML 형식으로 즉, 마크업 형식으로 정의하여 마크업을 반환하게 해준다.
  - 이러한 JS 함수 return 안에 마크업을 작성하는 문법을 React에서 **JSX**문법이라고 한다.

##  JSX
  - **JXS**란 위에서 서술한 것처럼 JS 파일 안에서 HTML과 유사한 마크업을 작성할 수 있는 확장 문법을 말한다.
  ```
  const MyComponent = () => {
    return(
        <h1>hello react!!</h1>
    )
  }
  ```
  - 이런식으로 JS 함수의 return 안에 작성하는 방식이며 만약에 작성할 마크업이 많다면 
  ```
  const MyComponent = () => {
    return(
      <div>
        <h1>hello react!!</h1>
        <p>hello react!!!</p>
        <p>hello react!!!!!</p>
      </div>
    )
  }
  ```
  - 위에 있는 코드처럼 하나의 부모 태그로 묶어야 한다. 묶지 않는다면 오류가 생기게 된다.
  ```
  const MyComponent = () => {
    return(
      <>
        <h1>hello react!!</h1>
        <p>hello react!!!</p>
        <p>hello react!!!!!</p>
      </>
    )
  }
  ```
  - 굳이 div 태그와 같은 의미 있는 태그를 사용하여 태그들울 묶을 필요없이 `<> </>`로 묶어줄 수 도 있다.
  - 특히  `<> </>`는 처음에 태그들을 묶어주는 역할만 할 뿐 실질적으로 저 태그는 없는 태그 취급이기 때문에 렌더링할 때 렌더링이 안된다.

## 한줄 정리
  - React는 UI를 컴포넌트 단위로 나누어 구현하는 JavaScript 라이브러리이다.
  - 컴포넌트란 하나의 작은 UI 조각를(예: 입력창, 버튼 등등...) 말한다.
  - JSX문법이란 JS 파일에서 HTML과 유사한 마크업 문법을 사용할 수 있는 확장 문법이다.