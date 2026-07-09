# React 기초2

## Props란?
  - Props란 서로다른 컴포넌트들이 서로 데이터를 주고 받을 수 있게 하는 일종의 함수의 매개변수와 같은 기능을 하는 변수를 말한다.
  ```
  export default function MyApp() {
    const [count, setCount] = useState(0);

    function handleClick() {
      setCount(count + 1);
    }

    return (
      <div>
        <h1>Counters that update together</h1>
        <MyButton count={count} onClick={handleClick} />
        <MyButton count={count} onClick={handleClick} />
      </div>
    );
  }
  
  function MyButton({ count, onClick }) {
    return (
      <button onClick={onClick}>
        Clicked {count} times
      </button>
    );
  }
  ```
  - 위 코드처럼 서로다른 컴포넌트끼리 데이터을 주고 받고 싶으면 데이터를 받는 컴포넌트는 JS함수에 매개변수를 정의하는 것처럼 컴포넌트 이름 뒤에 붙는 ()에 Props의 이름을 정의하면 되고
  - 정보을 주는 컴포넌트는 해당 컴포넌트 안에다 정의한 Props의 이름과 중괄호로 전달할 정보 즉, 변수의 이름을 작성하면 된다. 

## State란?
  - State란 각각의 컴포넌트가 값을 저장할 수 있게 해주는 저장공간(메모리)를 말한다.
  - State는 useState라는 React의 훅을 사용하여 정의하고 관리할 수 있다.
    - useState는 나중에 후술할 것이므로 이정도만 말하고 끝내겠다.
  ### State가 필요한 이유
  - State가 필요한 이유는 한마디로 설명하자면 **정보가 실시간으로 계속 변경 되기** 때문이다.
  - 즉, 웹사이트를 사용하다보면 여러가지로 정보를 입력을 받고 계속 정보가 수정된다.
  - 그렇지만 로그인 정보 또는 사용자가 입력한 사용자의 정보 같은 경우 계속 유지가 되어야 한다.
  - 이러한 입력받은 데이터를 유지하기 위해서는 어딘가에 저장을 해야하고 즉, 저장할 공간이 필요한데
  - 이러한 저장 공간의 역할을 바로 State가 맡아서 하는 것이다.

## 한줄 요약
  - Props란 서로다른 컴포넌트가 서로 정보를 넘기기 위해 사용하는 정보이다.
  - State는 각각의 컴포넌트가 입력한 정보를 저장하는 저장공간이다.
  - 즉 Props는 컴포넌트끼리 정보를 전달할 때 사용되는 정보를 의미하며 State는 컴포넌트가 입력한 정보를 저장하는 저장공간을 의미한다고 말할 수 있다.