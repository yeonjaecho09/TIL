# React의 UI
## 컴포넌트
  - 컴포넌트란 하나의 **독립된 UI 조각**을 뜻한다.
  ### 규칙
  - JS의 함수 형식을 작성해야한다.
  - 특히 컴포넌트의 이름은 첫문자가 대문자로 시작해야 하며, JSX 마크업을 반환해야 한다.
    - JSX 마크업을 반환하지 않으면 그냥 함수이다.
  ```
  const MyComponent = () => {
    return(
        <h1>hello react!!</h1>
    )
  }
  ```
  ---
  - 그리고 태그가 2개 이상일 경우 부모 태그로 묶어줘야 한다.
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
  - 그리고 굳이 `<div>`로 묶지 않아도 되며 `<></>` 아니면 `<fragment>`태그를 사용하여 태그를 묶어줘도 된다.
  - dfadfadfadfdfdafaadsfasfadsfasdfaasdfasdfadadfasdfasdfasddfadfaasdfasdfasdfasd