# react-state
state 

-useState

 → 중첩된 함수에서 사용하지 말것.

 → 일반 자바스크립트에서 hook을 호출하지 말것.(커스텀 hook에서는 사용 가능. 파일명에는 use로 무조건 시작해야한다.

 → props를 업데이트 해야하는 상황이면 setState를 받아서 자식 컴포넌트에서 props.setState('업데이트')를 하지말고 함수를 받아서 함수안에 값을 넣어서 부모 컴포넌트에서 업데이트 해야한다.

 → useState 초기값으로 props를 쓰지마라. state 값이 업데이트 되더라도 자식 컴포넌트가 랜더링이 안 될 수 있음

 → props를 받아서 state에 할당하고 싶다면 useEffect에 [props]값을 넣어서 setState를 한다. 

 → useState는 조건문과 반복문에 사용하는 것을 권장하지 않는다. useState는 비동기 처리로 동작을 하기 때문에 state값이 업데이트 될때, 순서와 무관하게 동작될 가능성이 크기 때문에 사용하지 않는것을 권한다.

 → setState({value: value +1}); // 잘못된 방법

 → setState(prevState=>({value: prevState.value +1})); // 옳은 방법

 → useState는 반드시 불변성을 지켜준다.(얇은 복사를 할것인지, 깊은 복사를 할 것인지 결정한다)

 → useState가 많아서 리랜더링 고려해야 하는건 useState 수십개가 됐을경우이지.. 10개 이하일 경우에는 useRef 등 사용하려고 코드를 복잡하게 고려할 필요 없음.
