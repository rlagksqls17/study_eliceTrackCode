# React  

### 디렉토리 구조 살펴보기  

```jsx
**./node_modules/** 

: npm을 이용해 설치한 패키지들 모음 

**./public** 

: 정적인 파일들을 모아놓는 곳 

**./src/** 

: 리액트 개발을 위한 파일들을 모아 놓는 곳 

**./.gitignore** 

: Git을 이용할 경우 불필요한 파일을 무시할 수 있도록 하는 설정파일 

**./package.json** 

: 프로젝트에 관한 정보와 사용하는 패키지들을 명세하는 파일 

**./README.md** 

: 내 프로젝트에 관한 설명을 작성하는 파일 
```

```js
// CSS나 import 하는 것 만으로 역할을 하는 라이브러리인 경우 패키지 명을 바로 import
import "패키지명" 

// 기본적으로 패키지를 불러와 활용할 때에는 할당할 이름을 작성 
import something from "패키지명" 
import Axios from "axios";

// 패키지 내의 일부 메소드나 변수만 가져올 때는 구조분해를 하여 가져옴 
import {a, b} from "패키지명" 

// 패키지에 default로 export 되는 객체가 존재하지 않을 경우 * as 이름으로 불러옴
import = as something from "패키지명"

// 별도의 CSS 파일을 작성 후 프로젝트에 적용하고 싶은 경우 사용
// import 시 style이 적용 됨  
import "./App.css"  
```

## jsx 정보

특징 

HTML 태그 내에 Javascript 연산 

class = 대신 className = 

### 중괄호 ({})

jsx 중괄호 안에는 여러 **자바스크립트 표현식**을 사용 가능  

```jsx
const expression = 3*5
const element = <h1>3*5= {expression}</h1>;
```

###  **스타일은 object로 {{ }}**  

```jsx
//HTML의 인라인 스타일은 ""(큰따옴표)로 감싼 string으로 정의하지만 React에서는 {}(중괄호)로 감싼 object로 정의합니다.  
const App = () => (
    <div style={{ 
        padding: 30,  
        color: "red", 
        backgroundColor: "blue" 
    }}>Hello world!</div>
)
```

```jsx
import React from 'react';
import './App.css';

function App() {
  return (
      // Class가 아닌 ClassName을 사용
    <div className="App">
        <div style = {{
        padding: 48,
        backgroundColor: "blue",
        color: "red"}}>안녕하세요.</div>
    </div>
  );
}

export default App;
```

```jsx
// 기존 JSX 문법 대신 React.createElement() 메소드 이용 가능  
// React에서 자동으로 코드 내 버그를 체크한다는 장점
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

닫는 태그 필수 />

###  **최상단 element는 반드시 하나**   

```jsx
// 함수
const App = () => {
    return(
    <> {/* React.Fragment */}
     <div>Hello</div>
     <div>World</div>
    </>
    )
};

// 변수  
const element = (
    <div>
        <h2>코더랜드에 오신것을 환영합니다:)</h2>
        <h2>즐거운 React! 함께 공부해봐요~</h2>
    </div>
);
```

## Component   

: React에서 페이지를 구성하는 최소단위 

: Component의 이름은 대문자로 시작 

### 1. Class Component

```jsx
// class Component
// 만들 때는 React.Component를 상속받고 render() 메소드를 구현해야 함  
class Clock extends React.Component {
  render() {
    return (
      <div>
        <h1>{this.props.date.toLocaleTimeString()}.</h1>
      </div>
    );
  }
}
```

### 2. Function Component

```jsx
// 화살표 함수  
const Hello = (props) => {
    const {name} = props
    return <div>{name}님 안녕하세요.</div>
}
// 기본 함수  
function Clock(props) {
  return (
    <div>
      <h1>{props.date.toLocaleTimeString()}.</h1>
    </div>
  );
}  
```

4. Controlled Component/Uncontrolled Component 

### 컴포넌트 합성  

```jsx
class Elice extends React.Component {
  render() {
    return <h2>I am a elice!</h2>;
  }
}

// Question 클래스에서 Elice 클래스를 참조 중
class Question extends React.Component {
  render() {
    return (
      <div>
      <h1>Who are you?</h1>
      <Elice />
      </div>
    );
  }
}

ReactDOM.render(<Question />, document.getElementById('root'));
```

## props  

```jsx
const MyComponent = (props) => {
    // 정의는 return 문 밖에서
    const { user, color, children } = props  
    
    return(
    	<div style={{ color }}>
        <p>{user.name}님의 하위 element는!</p>
            {children}
        </div>
    )
}

<MyComponent user = {{name: "민수"}} color= "blue">
<div>안녕하세요.</div>
</MyComponent>  

// 구조 분해 할당으로 간결하게 props를 받아오는 방법
const Welcome = (props) => {
    const { a, b, c } = props;
    return <div>...</div>
}
```



## Hook

**1. Hook : state와 event를 활용한 동적 렌더링**

```jsx
// const [<상태 값 저장 변수>, <상태 값 갱신 함수>] = userState(<상태 초깃값>);
import {useState} from 'react';

function Example(){
    // hook의 이름은 use로 시작
	const [inputValue, setInputValue] = 
          useState("defaultValue");
    const handleChange = (event) => {
        setInputValue(event.target.value);
    }
    return(
    	<div>
        	<input onChange = {handleChange}
                defaultValue = {inputValue}>
            </input>
            입력값 : {inputValue}
        </div>
    )
    
}
```

**2. Hook : object를 이용한 State**  

```jsx
// 오브젝트를 갖는 State를 만들 때 주의사항  
// 바로 object나 array 내부의 값만 변경할 경우 React가 새로운 값으로 변경된 것을 인지하지 못한다.
import { useState } from "react";

const [user, setUser] =
      useState({name:'민수', grade: 1})
	setUser((current) => {
        // 객체 복사
        const newUser = {...current}
        newUser.grade = 2
        return newUser
    })	
```

**3. Hook : object+ state + event**  

```jsx
const App = () => {
    const [user, setUser] = useState({ 
    	name: "민수",
        school: "엘리스대학교"
    });
    
    const handleChange = (event) => {
        const {name, value} = event.target;
        const newUser = {...user};
        newUser[name] = value;
        setUser(newUser);
    };
    
    return(
    	<div>
        	<input name = "name" 
                onChange = {handleChange}
                value = {user.name}>
            </input>
            <input name = "school"
                onChange = {handleChange}
                value = {user.school}>
            </input>
        </div>
    )
}
```

**4. 나만의 훅**

```jsx
const useUser = () => {
  // useState()를 이용해 state 변수를 만드세요.
  const [nickname, setNickname] = useState('')

  const updateNickname = event => {
    const nickname = event.target.value

    setNickname(nickname)
  }

  return [nickname, updateNickname]
}

const User = () => {
  // React Hook을 호출하세요.
  const [nickname, setNickname] = useUser('')

  return (
    <div>
      <label>{nickname}</label>
      <input value={nickname} onChange={setNickname} />
    </div>
  )
}
```

 

### Hook의 규칙  

```html
- 최상위에서만 Hook 호출    

: 반복문, 조건문, 중첩함수 내에 Hook 호출 금지  

: 따라서 React가 useState()와 useEffect()가 여러 번 호출되는 중에도 Hook의 상태를 올바르게 유지할 수 있도록 해줘야 함  

- 오직 React 함수 내에서 Hook을 호출해야 함  
- 또는 나만의 hook에서 hook 호출 가능

: 함수 컴포넌트에서만 Hook 호출  

> Hook 호출 순서에 React가 의존함
```

### useState

```html
단순한 하나의 상태를 관리하기에 적합함  
const [state, setState] = useState(initState | initFn)
state가 바뀌면, state를 사용하는 컴포넌트를 리렌더함  
useEffect와 함께 state에 반응하는 훅을 구축

상위 컴포넌트에서 state와 state 변경 함수를 정의하고,  
그 state나 변경 함수를 사용하는 컴포넌트까지 prop으로 내려주는 패턴  

state가 변경되면, 중간에 state를 넘기기만 하는 컴포넌트들도 모두 리렌더링 됨  

상태와 상태에 대한 변화가 단순하거나, 상대적으로 소규모 앱에서 사용하기 적합  
```



**1. Props와 state를 이용한 클래스 컴포넌트 지정**

```jsx
class Clock extends React.Component {
  // props, this.state를 지정
    // 불필요한 내부 데이터 은닉
  constructor(props) {
    super(props);
    this.state = {date: new Date()};
  }
  // 기존 클래스 함수
  render() {
    return (
      <div>
        <h1>{this.state.date.toLocaleTimeString()}.</h1>
      </div>
    );
  }
}

// 렌더링
ReactDOM.render(
  <Clock //원래 : date={new Date()} />,
  document.getElementById('root')
);
```

**2. 일반 인수를 이용한 State**

```jsx
// onClickEventHandler() 메소드가 호출되면 State의 name 데이터가 "엘리스 토끼"로 변경됨
onClickEventHandler = () => {
  this.setState({
    name: "엘리스 토끼"
  });
};
```

### useRef  

```html
상태가 바뀌어도 리렌더링 하지 않는 상태를 정의함  

즉, 상태가 UI의 변경과 관계없을 때 사용  
ex) setTimeout의 timerId 저장  

uncontrolled component의 상태를 조작하는 등, 리렌더링을 최소화하는 상태 관리에 사용됨  
ex) Dynamic Form 예시
```

### useContext  

```jsx
컴포넌트와 컴포넌트 간 상태를 공유할 때 사용 

부분적인 컴포넌트들의 상태 관리, 전체 앱의 상태 관리를 모두 구현  

Context Provider 안에서 랜더링 되는 컴포넌트는 useContext를 이용해 깊이 nested 된 컴포넌트라도 바로 context value를 가져옴  

context value가 바뀌면 내부 컴포넌트는 모두 리렌더링 됨  

Provider 단에서 상태를 정의하고, 직접 상태와 변경 함수를 사용하는 컴포넌트에서 useContext를 이용해 바로 상태를 가져와 사용하는 패턴  

useReducer와 함께, 복잡한 상태와 상태에 대한 변경 로직을 두 개 이상의 컴포넌트에서 활용하도록 구현 가능  

const TodoContext = createContext(null);

const initialState = {
    todos: [],
    filter: "all",
    globalId: 3000,
};

function useTodoContext(){
    const context = useContext(TodoContext);
    if (!context){
        throw new Error("rolem");
    }
    return context;
}

function TodoContextProvider({ children }){
    const values = useTodoState();
    return <TodoContextProvider
               value = {values}>
    	{children}
    </TodoContextProvider>
}

function reducer(state, action){
    switch (action.type){
        case "change.filter":
            return {...state, filter:
                   action.payload.filter};
        case "init.todos":
            return {...state, todos:
                   action.payload.todos};
        case "add.todo" : 
            return {...state, todos: [{title:
                action.payload.title, id: state.globalId + 1}]
        }
    }
}
```

### useReducer

```js
// useState 보다 복잡한 상태를 다룰 때 사용
// 별도의 라이브러리 없이 flux pattern에 기반한 상태 관리를 구현  
// 다음과 같이 선언
// setState 대신 dispatch 함수를 이용하여 reducer 함수에 type을 넘겨줌으로써 각각의 state를 설정함
const [<상태 객체>, <dispatch 함수>] = useReducer(<reducer 함수>, <초기 상태>, <초기 함수>)

import React, { useEffect, useReducer } from 'react';
import axios from 'axios';

// reducer() 함수를 완성하세요.
function reducer(state, action) {
    switch (action.type) {
        case 'LOADING':
            return {
                loading: true,
                data: [],
                error: null
            };
        case 'SUCCESS':
            return {
                loading: false,
                data: action.data,
                error: null                
            };
        case 'FAIL':
            return {
                loading: false,
                data: [],
                error: action.error
            };
        default:
            throw new Error();
    }
}

const initialUserState = {
  loading: false,
  data: [],
  error: null
}

function Users() {
    const [state, dispatch] = useReducer(reducer, initialUserState);
    
    async function fetchUser() {
        try {
            // dispatch를 이용해 state를 설정하는 코드입니다.
            dispatch({ type: 'LOADING' });
            const response = await axios.get(
                'https://jsonplaceholder.typicode.com/users'
            );
            dispatch({ type: 'SUCCESS', data: response.data });
        } catch (e) {
            dispatch({ type: 'FAIL', error: e });
        }
    };
    
    useEffect(() => {
        fetchUser();
    }, []);
    
    // useReducer의 state를 불러오는 코드입니다.
    const { loading, data, error } = state;
    
    if(loading)
        return <h4>로딩중...</h4>;
    if(error)
        return <h4>에러 발생!</h4>;
    
    const userName = data.map(
        (user) => (<li key={user.id}> {user.name} </li>)
    );
    
    return (
        <>
            <h4>사용자 리스트</h4>
            <div> {userName} </div>
            <button onClick={fetchUser}>다시 불러오기</button>
        </>
    );
}

export default Users;

nested state등 복잡한 여러 개의 상태를 한꺼번에 관리하거나 어떤 상태에 여러 가지 처리를 적용할 때 유용  

상태가 복잡하다면, useState에 관한 callback을 내려주는 것보다 dispatch를 prop으로 내려 리렌더링을 최적화하는 것을 권장
```

```jsx
// App.js

import React, {useState, useEffect} from 'react';
import {Provider, useDispatch, useSelector} from "react-redux";
import store from "./redux/store"
import {increment} from "./redux/action"

function Count2() {
  // 액션을 전달할 필요가 없기 때문에 dispatch를 사용 안함
  const count = useSelector((state) => state.count);
  return (
    <p>{count}</p>
  )
}

// state를 전역으로 가져오는 Reducer
function Count(){
  // 액션을 리듀서로 전달
  const dispatch = useDispatch();
  // initstate를 가져옴 (스토어가 설명을 위해 생략 됨)
  const count = useSelector((state) => state.count);

  const handleClick = () => {
    // setState와 비슷한 역할
    dispatch(increment());
  }

  return (
    <div>
      <button onClick = {handleClick}>증가</button>
      <p>카운트 : {count}</p>
    </div>
  )
}

function App(){
  return (
    // Provider 안에 있는 컴포넌트들만 dispatch와 selector를 사용할 수 있음
    <Provider store = {store}>
      <div className = "App">
        <Count />
        <Count2 />
      </div>
    </Provider>
  )
}

export default App;

// reducer.js  

const initState = {
    count: 0
}

const Reducer = (state = initState, action) => {
    switch(action.type) {
        case "INCREMENT":
            return {
                count: state.count + 1
            }
        default:
            return state;
    }
}

export default Reducer;

// action.js  

export const increment = () => {
    return {
        type: "INCREMENT",
    }
}

// store.js  

import {createStore} from 'redux';
import Reducer from "./reducer"

const store = craeteStore(Reducer)

export default store;
```



### Effect Hook  

함수형 컴포넌트에서 side effects들을 실행하는 것  

```jsx
import { useEffect } from 'react';
// EffectCallback : Deps에 지정된 변수가 변경될 때 실행할 함수
// Deps : 변경을 감지할 변수들의 집합  
const App = () => {
    useEffect(EffectCallback, [Deps?])
}
// Deps에 아무것도 안 넘겨주면 컴포넌트의 생성과 소멸 시에만 Effect Callback 함수가 호출됨
// useEffect의 이펙트 함수 내에서 다른 함수를 return 할 경우 state가 변경되어 컴포넌트가 다시 렌더링되기 전과 컴포넌트가 없어질 때 호출할 함수를 지정하게 됨
const App = () => {
    
    useEffect(() => {
        console.log("컴포넌트 생성");
        
        return () => {
            console.log("컴포넌트 소멸");
        }
    }, 
    []);
    return <div></div>
}
```



React 컴포넌트 안에서 **데이터를 가져오거나 구독하고, DOM을 직접 조작하는 작업을 side effects라고 함**. 이러한 과정은 다른 컴포넌트에 영향을 줄 수도 있어 렌더링과정에서는 구현불가  

Effect Hook의 useEffect()는 함수형 컴포넌트 내에서 이런 side effects를 수행할 수 있게 해줌  

즉 지정한 State나 Prop가 변경될 때마다 이펙트 콜백 함수가 호출됨

버튼 클릭 대마다 1씩 카운트를 하는 카운터 컴포넌트에서 매 렌더링, State 업데이트 시에 count를 갱신하고 싶을 때  

**componentDidMount()** 와 **componentDidUpdate()**를 사용  

```jsx
import React, { useState, useEffet } from 'react';

const Example = () => {
    const [count, setCount] = useState(0);
    // 모든 렌더링 요소마다 원하는 작업 수행 가능하여 
    // 코드 중복할 필요가 없음
    // 생명주기 메소드 사용할 필요 없음
    // EffectCallback : Deps에 지정된 변수가 변경될 때 실행할 함수
// Deps : 변경을 감지할 변수들의 집합
    useEffect() => {
        document.title = `You cheked ${count} times`, count
    }
    
    return(
    	<div>
        	<p> you clicked {count} times </p>
            <button onClick={() => setCount(count + 1)}> Click Me</button>
        </div>
    )
}
```

#### useMemo  

지정한 State나 Props가 변경될 경우 해당 값을 활용해 계산된 값을 메모이제이션 하여 제 랜더링 시 불필요한 연산을 줄임

```jsx
import React, {useState, useMemo} from 'react';

// 지속적으로 메모리를 쓰기 때문에 성능하락 이슈가 있을 수 있음
const App = () => {
    const [firstName, setFirstName] = useState('철수')
    const [lastName, setLastName] = useState('김')
    
    const fullName = useMemo(() => {
        return `${firstName} ${lastName}`
    }, [FirstName, lastName])
}

```

#### useCallback  

함수를 메모이제이션하기 위해 사용하는 Hook이다. 컴포넌트가 재렌더링될 때 불필요하게 **함수가 다시 생성되는 것을 방지**한다. 

**시간이 걸리는 Return**  

```jsx
// 지속적으로 메모리를 쓰기 때문에 성능하락 이슈가 있을 수 있음
const App = () => {
    const [firstName, setFirstName] = useState('철수')
    const [lastName, setLastName] = useState('김')
    
    // 이름과 성이 바뀔 때마다 풀네임을 return하는 함수를 메모이제이션  
    const getFullName = useCallback(() => {
        return `${firstName} ${lastName}`
    }, [firstName, lastName])
    
    return <>{getFuallName()}</>
}
```

## Promise  

```jsx
// Promise : 비동기 처리에서 사용되는 객체, Promise가 상태를 관리함  

/*resolve : 로직이 성공 시 실행하면 fulfilled(이행) 상태가 되게 해주는 callback함수임  

reject : 로직이 실패하였을 때 실행하면 rejected 상태가 되게 해주는 callback 함수임*/

function getUser(id) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Reading from a database....");
			if(id !== 1){
				reject("User not found!");
			}
      resolve({ id: id, username : "test" });
    }, 2000);
  });
}


getUser(1)
	.then((user)=>{
		console.log(user);
	})
	.catch((e)=>{
		console.error(e);
	});
```

### Async/Await  

es6에서 나온 개념  

then을 통한 chaining 제거  

promise 반환하는 함수 앞에 await을 명시  

async함수는 항상 promise 함수 반환  

```jsx
// resolve는 코드를 이행하는 것 
	// ('resolved') 반환
function resolveAfter2Seconds() {
  return new Promise(resolve => {
    setTimeout(() => {
      resolve('resolved');
    }, 2000);
  });
}

// 코드 실행 후 asyncCall에는 Calling 을 콘솔창에 출력한 뒤, 2초 후 resolved를 출력함  
	// async는 함수 이름 부분의 제일 앞에,
	// await는 결과를 기다릴 함수 호출 부분 앞에 작성함

// async : 해당 함수에서 비동기 처리를 위한 Promise 동작을 한다는 것을 명시  
// await : 호출되는 함수가 적절한 결과를 반환할 때까지 기다림
	// await을 사용하기 위해 async를 명시해야 함
async function asyncCall() {
  console.log('calling');
  const result = await resolveAfter2Seconds();
  console.log(result);
}

asyncCall();
```

### axios  

```jsx
import axios from 'axios';
// 동기방식
axios.get('request url')
	.then(
	(response) => {
     	console.log("받아온 데이터", response.data)   
    })

// 비동기방식
axios.get(`요청할 url 1`)
  .then(res => axios.get(`요청할 url 2`))
  .then(res => {
    const ps = res.data.map(user => axios.get(`요청할 url 3`));
    ···
  })
  .then(ress => ···)))
  .then(repoArrs => {
    ···
    }
    ···
  })
// 근데 이런걸 콜백 지옥이라함. 이 콜백지옥을 벗어나기 위해 async와 await을 이용할 수 있음 (위에 있음)
  
  import React, { useState, useEffect } from 'react';
import axios from 'axios';

function Users() {
    const [users, setUsers] = useState([]);
    const [error, setError] = useState(null);
    
    useEffect(() => {
        async function fetchUser() {
            // try ~ catch를 이용해 예외 처리를 하세요.
            const response = await axios.get(
                'https://jsonplaceholder.typicode.com/error'
            );
            setUsers(response.data);
        };
        fetchUser();
    }, []);
    
    const userName = users.map(
        (user) => (<li key={user.id}> {user.name} </li>)
    );

    if (error) return <h4>에러 발생!</h4>;
    return (
        <>
            <h4>사용자 리스트</h4>
            <div> {userName} </div>
        </>
    );
}

export default Users;

```



### fetch  

```jsx
// API를 사용하여 백엔드 서버와 비동기 요청을 하는 방식 중 하나

let promise = fetch(url, [options])
```



## useRef  

컴포넌트 생애 주기 내에서 유지할 ref 객체를 반환

ref 객체가 변경이 되더라도 다시 렌더링하지 않게 하도록 함

```jsx
const App = () => {
    const inputRef = useRef(null)
    const onButtonClick = () => {
        inputRef.current.focus()
    }
    return (
    	<div>
        	<input ref = {inputRef} type = "text">
            	<button onClick = {onButtonClick}>
                    input으로 포커스
                </button>
            </input>
        </div>
    )
}
```







## Element

엘리멘트란 React 앱의 가장 작은 단위를 말함  

### Render 와 ReactDOM

```jsx
// App.js
const name = 'Josh Perez';
const element = <h1>Hello, {name}</h1>;

// id가 root인 태그를 찾은 후, 정의한 엘리먼트를 ReactDOM에 렌더링
ReactDOM.render(element,document.getElementById('root'));
```

```html
<!--index.html-->
<div id = "root"></div>
```

### 생명주기  메소드

React의 생명 주기는 컴포넌트가 이벤트를 다룰 수 있는 특정 시점을 말함  

**마운트** : 컴퓨터가 실제 DOM에 삽입 되는 것 

**업데이트** : 컴포넌트가 변하는 것  

**언마운트** : 컴포넌트가 DOM 상에서 제거되는 것

#### constructor() 

State 데이터를 초기화 하는 메소드

#### render()

클래스 컴포넌트에서 반드시 구현되어야 하는 메소드  

#### componentDidMount()

컴포넌트가 마운트 된 직후 호출되는 메소드

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
  }
  // setTimeout 이용해서 타이머를 실행
  // 현재 코드를 실행하면 처음에는 red가 표시되다가 1초 뒤에 yellow로 변하게 됨
  componentDidMount() {
    setTimeout(() => {
      this.setState({favoritecolor: "yellow"})
    }, 1000)
  }
  render() {
    return (
      <h1>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}

ReactDOM.render(<Header />, document.getElementById('root'));
```



#### componentDidUpdate()

업데이트가 진행된 직후에 호출되는 메소드  

#### componentWillUnmount()  

컴포넌트가 마운트 해제되어 제거되기 직전에 호출되는 메소드

#### export

```jsx
export default Student;
```



**예제 코드 1**  

```jsx
// App.js  
import React from 'react';
import './App.css';
import Welcome from './components/Welcome'

function App() {
  return (
    <div className="App">
        <Welcome />
    </div>
  );
}

export default App;


// Welcome.js
import React from "react";

const Welcome = () => {
    const username = "철수";
    
    return(
        <h1>{username}님 안녕하세요.</h1>
    )
}

export default Welcome;
```

**예제 코드2**

```jsx
//버튼 클릭된 횟수를 저장
let value = 0


//버튼 클릭시 횟수를 증가시키는 함수를 정의합니다.
function click() {
  value += 1;
}


function tick(){
  const element = (
    <div>
      <h1>버튼을 클릭해보세요</h1>
      <button onClick={click}>Click Me!</button>
      <h2>총 {value}번 클릭했습니다.</h2>
    </div>
  );
  
  //ReactDOM과 element를 렌더링합니다.
  ReactDOM.render(element, document.getElementById('root'));
  
}

//1초마다 tick()함수 호출
setInterval(tick, 1000);

serviceWorker.unregister();
```



## 이벤트  

1.리액트에서 이벤트의 이름은 카멜(Camel) 표기법으로 사용  

2.이벤트에 실행할 코드 전달(X) 함수 형태의 객체 전달(O)

```jsx
<input type = "text"
    name = "message"
    placeholder = "input message"
    // 이벤트 이름은 카멜 표기법으로 사용
    onChange = {
        // 이벤트를 실행할 코드를 그대로 전달하는 것이 아니라 아래 onClick 처럼 함수의 형태로 객체 전달
        // onChange = {함수명}
        (e) => {
            console.log(e.target.value)
        }
    }
```

3. 직접 만든 리액트 컴포넌트에는 이벤트를 자체적으로 설정할 수 없음 (<div><button><p><input>)  

```jsx
// 안 되는 예제 코드  
render() {
    return (
        <EventPractice onLoad={
            ()=>{
            console.log("test");
            }
        }/>
    );
}
```

### 이벤트 등록

**1. 함수형 컴포넌트에 이벤트 정의**  

예제코드 1 : onClick

```jsx
function ActionLink(){ // 컴포넌트
	// 등록 부분
    function handleClick(e){
        console.log('The link was clicked');
    }
    // 이벤트 호출 부분
	return (
	<a href= "#" onClick = {handleClick}>
	 Click me    
	</a>
		);
}
```

예제코드 2: onChange, event.target.value 

```jsx
const App =() =>{
    const handleChange = (event) =>{
        console.log(event.target.value + "라고 입력")
    }
	return (
		<div>
    		<input onChange = {handleChange} />
    	</div>
		)
}
```



**2. 클래스형 컴포넌트에 이벤트 정의 (props 포함)**  

```jsx
class Header extends React.Component {
  constructor(props) {
    super(props);
    this.state = {favoritecolor: "red"};
 // 1. 이벤트 바인딩
     this.이벤트명 = this.이벤트명.bind(this);
  }
    
// 2. 이벤트 정의  
    이벤트 명 = () =>{
        
    }
    
// 3. 이벤트 호출
  render() {
    return (
      <h1 onClick = {this.이벤트명}>My Favorite Color is {this.state.favoritecolor}</h1>
    );
  }
}
```

**3. 클래스인데 props 따로 지정 안할 시 유용한 코드** 

```jsx
import React from "react";

export default class Example2 extends React.Component {
  state = {
    text: "텍스트",
  };

  handleChange = (e) => {  // <- input값으로 text 변경 함수
    this.setState({
      text: e.target.value,
    });
  };

  render() {
    return (
      <div>
        <input onChange={this.handleChange} /> // <-변경된 곳
        <h1>{this.state.text}</h1>
      </div>
    );
  }
}
```

**4. 함수 안에 이벤트 등록**

```jsx
 <button onClick={
        () => {
            alert(this.state.message)
            this.setState({
                message : ''
            })
        }
    }>
</button>
```

### 인수 전달후 이벤트 등록

```jsx
// id 값을 추가 인수로 전달해야 하는 경우  
// e : React 이벤트를 나타내는 인자
<button onClick={(e) => this.이벤트명(매개변수, e)}></button>
// bind를 사용하는 경우 e를 따로 전달해주지 않아도 됨
// 명시적으로 bind 지정 필요
<button onClick={this.이벤트명.bind(this, 매개변수)}></button>

// 예제 코드  
class EventClass extends React.Component {
  constructor(props) {
    super(props);
    // binding이 필요없음
  }

  //handleClick 이벤트를 정의합니다. 인자값을 받아 alert()을 출력합니다.
  const handleClick = (data) => {
    alert(`전달받은 인자값: ${data}`)
  }


  render() {
    var data = "ABCDEFG"
    return (
      //data값을 인자값으로 제공하는 이벤트 핸들러를 작성합니다. 
      <button onClick = {(e) => this.handleClick(data,e)}>
        버튼을 눌러주세요!
      </button>
    );
  }
}
```

### 상위 컴포넌트에 이벤트 등록  

```jsx
// props로 onchange 함수 등록  
const MyForm = ({ onChange }) => {
    return(
    	<div>
        	<span>이름: </span>
            <input onChange={onChange} />
        </div>
    )
}

// 상속 주는 컴포넌트  
// props도 가능 
const App = () => {
    const [username, setUsername] = useState('')
    return (
    	<div>
        	<h1>
            	{username}님 환영합니다.
            </h1>
            <MyForm 
                onChange = {(event) => {
                    setUsername(event.target.value)
                }} />
        </div>
    )
}
```



## 조건부 렌더링  

```jsx
// 1
function Greeting(props) { //인사하는 컴포넌트 선언
  const isLoggedIn = props.isLoggedIn; //props에서 받아온 isLoggedIn값을 inLoggedIn 변수에 할당
  if (isLoggedIn) { //할당한 변수의 값을 if문으로 확인 (= 조건별로 구분하기)
    return <UserGreeting /> //true일 때 실행되는 컴포넌트
  }
  return <GuestGreeting /> //false일 때 실행되는 컴포넌트

  ReactDOM.render(
    //isLoggedIn={true}; 로 하면 어떤 컴포넌트가 실행될지 생각해보세요!
    <Greeting isLoggedIn={false} />, //Greeting이라는 컴포넌트를 불러올 때, isLoggedIn이라는 props를 주고, props의 false 값을 할당합니다.
    document.getElementById('root')
  );
}

// 2  
class LoginControl extends React.component {
  constructor(props) {
    super(props)
    this.handleLoginClick = this.handleLoginClick.bind(this);
    this.handleLogoutClick = this.handleLogoutClick.bind(this);
    this.state = {isLoggedIn: false};
  }

  handleLoginClick() {
    this.setState({isLoggedIn: true})
  }

  handleLogoutClick() {
    this.setState({isLoggedIn: false})
  }

  render() {
    const isLoggedIn = this.state.isLoggedIn;
    let button; //버튼 변수 선언 (바로, 이 변수가 element variables 입니다.) 컴포넌트를 이 변수에 할당할 수 있다는 의미입니다. (어려운 개념이 아니니, 겁 먹지 마세요!)

    if(isLoggedIn) {
      button = <LogoutButton onClick={this.handleLogoutClick} />; //로그인 상태일 경우, button변수에 LogoutButton 엘리먼트를 할당
    } else {
      button = <LoginButton onClick={this.handleLoginClick} />; //로그 아웃 상태일 경우, button변수에 LoginButton 엘리먼트를 할당
    }

    return (
      <div>
        <Greeting isLoggedIn={isLoggedIn} /> //Greeting 컴포넌트를 보여주고 있다.
        {button} //button 엘리먼트를 렌더링하고 있다.
      </div>
    )
  }
}

ReactDOM.render(
  <LoginControl />,
  document.getElementById('root')
);

// 3. JSX로 구현하기  
function Mailbox(props) { //Mailbox라는 function component 선언
  const unreadMessages = props.unreadMessages; //읽지 않은 메세지 값을 받아 unreadMessages 변수에 할당
/* 조건부 렌더링 부분! */
  return (
    <div>
      <h1>Hello!</h1>
            /*이 부분이 true이면 렌더링, false면 렌더링 하지 않는다.*/
      {unreadMessages.length > 0 && /* unreadMessages 의 길이가 0보다 크면 아래 <h2> 태그를 렌더링 */
        <h2>
          You have {unreadMessages.length} unread messages.
        </h2>
      }
    </div>
  );
}

const messages = ['React', 'Re: React', 'Re:Re: React']; //messages 배열에 3가지 값을 담았습니다.
ReactDOM.render(
  <Mailbox unreadMessages={messages} />, // props 값을 받는다.
  document.getElementById('root')
);

// 4. 
render() {
  const isLoggedIn = this.state.isLoggedIn;
  return (
    <div>
            {/* 중괄호 안에서 isLoggedIn이 true이며 LogoutButton 컴포넌트를 렌더링, false면 LoginButton 컴포넌트를 렌더링 */}
      {isLoggedIn ? ( 
        <LogoutButton onClick={this.handleLogoutClick} />
      ) : (
        <LoginButton onClick={this.handleLoginClick} />
      )}
    </div>
  );
}
```

#### &&  

```jsx
expr1 && expr2 // expr1이 true값을 반환할 수 있으면 expr2를 반환하고, 그렇지 않으면 expr1을 반환합니다.
true && expr // expr을 반환합니다.
false && expr // false를 반환합니다.
```

#### ?

```jsx
(조건) ? expr1 : expr2

function Check(props){
//Check의 props를 변수에 저장합니다.
  const data = parseInt(props.num);
  return(
    <div>
      <h2>{data > 0 ? "양수입니다" : "양수가 아닙니다."}</h2>

    </div>
  )
}
// 예제코드 2
    <div className="App">
        <button onClick={() =>
        {
            toggle();
        }}>
            {isOn ? "켜짐" : "꺼짐"}
        </button>
    </div>
```

#### e.preventDefault()

React에서 이벤트가 실행될 때, 페이지가 자동으로 새로고침 되는데 이를 방지하기 위해서임   

```jsx
//<a href ="#">는 링크를 설정하지 않은 상태이기 때문에 현재 페이지로 이동하여 새로고침 된다. 이를 방지하는 것이 e.preventDefault()
<a href="#" onClick={handleClick}>
    Click me
</a>  

function handleClick(e) {
    e.preventDefault();
    console.log('The link was clicked.');
}
```

# 백엔드  

### form과 props 이용한 등록과 초기화 구현

```jsx
//// App.js  
import React, { useState } from 'react';
import InsertForm from "./components/InsertForm";
import ListView from "./components/ListView";

function App() {
  const [todoList, setTodoList] = useState([]);
  
  const handleInsert = (value) => {
    setTodoList((current) => {
      const newList = [...current];
      newList.push({
        key: new Date().getTime(),
        value,
        isCompleted: false,
      });
      return newList;
    })
  }
  
  const handleComplete = (index) => {
    setTodoList((current) => {
      const newList = [...current];
      newList[index].isCompleted = true;
      return newList;
    })
  }
  
  const handleRemove = (index) => {
    setTodoList((current) => {
      const newList = [...current];
      newList.splice(index, 1);
      return newList;
    })
  }
  
  return (
    <div className="App">
        <ListView todoList={todoList} onComplete={handleComplete} onRemove={handleRemove} />
        <InsertForm onInsert={handleInsert} />
    </div>
  );
}

export default App;


//// InsertForm.js
import React, { useState, useCallback } from "react";

const InsertForm = ({ onInsert }) => {
    const [inputValue, setInputValue] = useState("");
    const handleSubmit = useCallback((event) => {
        event.preventDefault(); // 기본적인 HTML 동작으로 인해 페이지가 새로고침 되는 것을 방지
        if(typeof onInsert === "function" && inputValue) { // onInsert가 정상적인 함수인 지 확인하여 에러 방지
            onInsert(inputValue);
        }
        setInputValue("");
    },[onInsert, inputValue])

    return (
        <form onSubmit={handleSubmit}>
            <input value={inputValue} onChange={(event) => {
                setInputValue(event.target.value);
            }} />
            <button type="submit">등록</button>
        </form>
    )

}

export default InsertForm;

// ListView.js
import React from "react";

const ListView = ({todoList, onComplete, onRemove}) => {
  return (
    <div>
      <ol>
        {todoList.map((item, index) => {
          return (
            <li key={item.key}>
              <span>{item.value}</span>
              <button type="button" onClick={() => {
                if(typeof onComplete === "function") {
                  onComplete(index);
                }
              }}>완료</button>
              <button type="button" onClick={() => {
                if(typeof onRemove === "function") {
                  onRemove(index);
                }
              }}>삭제</button>
            </li>
          );
        })}
      </ol>
    </div>
  )

}

export default ListView;
```

### CSS 추가  

```jsx
import React, { useState, useCallback } from "react";

const InsertForm = ({ onInsert }) => {
    const [inputValue, setInputValue] = useState("");
    const handleSubmit = useCallback((event) => {
        event.preventDefault(); // 기본적인 HTML 동작으로 인해 페이지가 새로고침 되는 것을 방지
        if(typeof onInsert === "function" && inputValue) { // onInsert가 정상적인 함수인 지 확인하여 에러 방지
            onInsert(inputValue);
        }
        setInputValue("");
    },[onInsert, inputValue])

    return (
        <form onSubmit={handleSubmit} style={{
            baackgroundColor: "#ffffff",
            borderRadius: 16,
            marginBottom: 16,
            display: "flex",
            justifyContent: "space-between",
            alignItems: "center"
        }}>
            <input value={inputValue} onChange={(event) => {
                setInputValue(event.target.value);
            }} style={{
             flex: 1,
             border: "none",
             color: "#000000",
             padding: "6px 12px",
             backgroundColor: "transparent"
            }}/>
            <button type="submit" style={{
                border: "none",
                borderRadius: 16,
                backgroundColor: "#3ab6bc",
                color: "#ffffff",
                cursor: "pointer",
                padding: "8px 16px"
            }}>등록</button>
        </form>
    )

}

export default InsertForm;

```

### SPA  

```
**브라우저에서 빌드함**

하나의 페이지 요청으로 전체 웹앱을 사용하는 방식  

자체적으로 데이터를 갖고, 서버와의 동기화가 필요한 데이터만을 처리

SPA는 서버에 매번 요청을 하지 않고, 단 한 번만 페이지를 받아 페이지 관련 네트워크 요청이 줄어든다.

SPA는 단 하나의 페이지를 관리하며, 모든 라우트에서 해당 페이지를 내려주는 방식이다.

SPA는 모바일 앱을 사용하는 듯한 경험을 주기 위해 자바스크립트와 History API 등의 Web API를 이용, 페이지 리로드 없는 네비게이션을 구현한다.

SPA는 페이지 요청 시 주로 빈 페이지를 전송하므로, 서버에서 모든 페이지 정보를 렌더링하는 방식의 MPA보다는 Search Engine Optimization에 불리하다.
```

### MPA 

```html
**서버에서 빌드함**

서버에 미리 여러 페이지를 두고 유저가 네비게이션 시 요청에 적합한 페이지를 전달
MPA에서는 서버의 데이터를 이용해 패이지를 렌더링하므로, 클라이언트의 데이터와 서버의 데이터가 큰 차이를 가지지 않음
```



### react-router  

**설명**

Declarative routing for React

React의 JSX를 이용하거나, History API를 사용하여 라우팅을 구현

웹에서는 react-router-dom을 사용  

**적용 시, 서버의 모든 path에서 같은 앱을 서빙하도록** 해야 함. React 컴포넌트를 특정 path와 연결하면, **해당하는 path로 진입 시 컴포넌트를 렌더링** 하게 함.  

query, path variable 등 URL parameter를 얻어 활용함  

조건에 맞지 않을 경우 redirect함  

페이지 이동 시 이벤트 핸들러를 등록함  

/posts/my-post-1 등의 nested route를 구현함  

**사용법**  

#### BrowserRouter 컴포넌트

\<BrowserRouter\>로 감싸 Router Context를 제공해야 함  

HTML5의 History API를 사용하여, UI와 URL의 싱크를 맞추는 역할

#### Route 컴포넌트

**path와 컴포넌트를 매칭함**

Link로 특정 페이지로 이동 시 리로드 없이 페이지가 이동함  

Switch로, 매칭되는 라우트 하나를 렌더링하게 함

```jsx
function LoginPageContent(){
    // 비밀번호와 아이디가 올바르게 입력되었다고 가정하고 메인페이지로 이동
    const handleClickLogin = (e) =>{
        window.location.href="/"
    }
    const handleClickJoin = (e) =>{
        window.location.href="/join"
    }
    return(
        <div>
            <h1>로그인 페이지</h1>
            <button onClick={handleClickLogin}>
                로그인
            </button>
            <button onClick={handleClickJoin}>
                회원가입하기
            </button>
        </div>
    )
}

function LoginPage(){
    return(
        <Router>
            <div>
                <Switch>
                    <Route path = "/login">
                        <LoginPageContent />
                    </Route>
                    <Route path = "/join">
                        <JoinPage />
                    </Route>
                    <Route path = "/">
                        <MainPage />
                    </Route>
                </Switch>
            </div>
        </Router>
    )
}
```



#### Redirect 컴포넌트  

Link와 비슷하나 렌더링 되면 to prop으로 지정한 path로 이동함  

Switch 안에서 쓰일 경우 from, to를 받아 이동하게 만듦

#### Link, NavLink 컴포넌트  

to prop을 특정 URL로 받아, 클릭 시 네비게이션 함  

anchor tag를 래핑함  

NavLink의 경우, 매칭 시 어떤 스타일을 가질지 등의 추가 기능이 있음  

to에 location object나 함수를 받을 수 있음

#### useHistory, useLocation, useParams, useRouteMatch  

최상위 컴포넌트가 아니더라도, hook으로 react-router 관련 객체에 접근할 수 있음, history, location, params, match 객체에 접근함

```jsx
import { BrowserRouter, Route, Switch } from 'react-router-dom'  
export function App(){
    return(
    	<BrowserRouter>
        	<Switch>
            	<Route path="/about"><AboutPage/></Route>
                <Route path="/contact"><AboutPage/></Route>
                // 홈페이지는 항상 밑에 두기
                // Switch는 가장 위의 매칭되는 path의 컴포넌트를 렌더링한다.
                <Route path="/"><AboutPage/></Route>
            </Switch>
        </BrowserRouter>
    )
}
```

#### private Route  

특정 조건이 충족되지 않았을 때 다른 페이지로 Redirect하도록 하는 기능, 유저의 상세페이지, 개인정보 변경 페이지 등을 만들 때 사용됨  

```jsx
// 누가 보면 안되기 때문에 PrivateRoute로 감싸줌
function PrivateRoute({component: Component, ...props}){
    return <Route {...props} render = {props => {
            // !! 는 유효한 값인지 확인
            const isLoggedIn = !!getUserInfo()
            
            if (!isLoggedIn){
                return <Redirefct to="/login" />
            }
            return <Component {...props} />
        }}
}
```

#### query string 활용하기  

```jsx
function ContactPage(){
    const location = useLocation();
    const searchParams = new URLSearchParams(location.search);
    const email = searchParams.get("email")
    const address = searchParams.get("address")
    
    return (
    	<PageLayout header = "Contact Page">
        	<em>{email}</em>
            <br />
            <strong>{address}</strong>
        </PageLayout>
    )
}
```

```python
/*
위치포인트를 0에서 시작
    거리를 담은 사전을 준비해둠
    {
        1: 1
        3: 3
        7: 7
        10: 10
        11: 11
    }
    
    while(위치포인트 1에서 끝까지)
        위치포인트가 사전의 key값보다 작은값들은 모두 1씩 감소
        위치포인트가 사전의 key값보다 큰값들은 모두 1씩 증가
        이후 사전의 값의 sum 값을 구해서 최솟값을 갱신
    
*/
```



## 예제 코드

### 유저 데이터를 비동기로 요청해 렌더링하기

```jsx
// BitcoinApp.jsx  
import React, { useState, useEffect } from "react";
import styled from "styled-components";
import UserDetail from "./UserDetail";
// auth.js 파일에서 모든 코드를 import  
import * as authAPI from '../service/auth'

// style을 위한 컴포넌트
const WrappedUserDetail = styled(UserDetail)`
  & + & {
    margin-top: 12px;
  }
`;

// 유저 정보를 받아온 정보를 UserDetail에 넘겨 화면에 출력하세요.
// 데이터가 로딩 중인 경우 유저 정보를 불러오고 있다는 안내문을 띄웁니다.
export default function BitcoinApp() {
    // State 설정 
  const [ users, setUsers ] = useState(undefined)
    // 컴포넌트 생성 시에 authoAPI.getUsers()에서 데이터를 불러옴
  useEffect(() => {
    authAPI
        .getUsers()
      // 성공시 users 상태를 불러온 데이터로 변경함
        .then(setUsers)
  }, [])
  
  return (
    <div>
        {!users ? (
            <div>유저 정보를 로딩중입니다.</div>
        ) : users.map(user => (        
              // 받아온 데이터가 배열이므로, 배열 별 map으로 html코드써서 출력해줌
        <WrappedUserDetail 
            email={user.email}
            bitcoinAddress={user.bitcoinAddress}
            bitcoinBalance={user.bitcoinBalance}
        />
        ))
        }
    </div>
  );
}

// UserDetail.jsx
import React from "react";
import styled from "styled-components";
import { colors } from "../style/colors";

export default function UserDetail({
  email,
  bitcoinAddress,
  bitcoinBalance,
  className,
}) {
  return (
    <Container className={className}>
      <Email>
        <h4>Email</h4>
        <span>{email}</span>
      </Email>

      <Bitcoin>
        <div>
          <strong className="title">Bitcoin Address</strong>
          <span className="content">{bitcoinAddress}</span>
        </div>

        <div>
          <strong className="title">Bitcoin Balance</strong>
          <span className="content">{bitcoinBalance} BTC</span>
        </div>
      </Bitcoin>
    </Container>
  );
}

const Container = styled.div`
  display: flex;
  flex-direction: column;
  background: ${colors.pink0};

  width: 500px;
  padding: 24px;

  border-radius: 10px;
`;

const Email = styled.div`
    display: flex;
    
    h4 {
        margin: 0;
        font-size: 18px;
        font-weight: bold;
        width: 120px;
    }
    
    span {
        font-size: 14px;
        align-self: flex-end;
    }
`;

const Bitcoin = styled.div`
    .title{
        width: 120px;
        diplay: inline-block;
        
        font-size: 14px;
    }
    .content{
        font-size: 12px;
    }
`;

// App.js
import React from 'react';
import "./App.css";
import BitcoinApp from "./BitcoinApp/BitcoinApp";
import styled from "styled-components";

const Container = styled.div`
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
`;

function App() {
  return (
    <Container>
      <BitcoinApp />
    </Container>
  );
}

export default App;

// auth.js  
import { db } from "./db";
	// bitcoinApp.jsx에서 요청하는 getUsers는 db.getUsers()함수를 불러옴
export const getUsers = () => db.getUsers();

export const loginUser = ({ email, password }) => db.findUser(email, password);

export const registerUser = ({ email, password }) =>
  db.addUser(email, password);

// db.js
const delayedResolve = (data) =>
  new Promise((resolve, reject) => setTimeout(() => resolve(data), 250));

const bitcoinAddressBuilder = (() => {
  const possibleCharacters =
    "1234567890ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz";

  const generateRandomNumber = (max, min = 0) =>
    Math.floor(Math.random() * (max - min + 1)) + min;

  // P2PKH invoice address format
  const generateBitcoinAddress = () => {
    const selectionLength = possibleCharacters.length - 1;
    const addressLength = generateRandomNumber(34, 25);

    const generatedAddress = "1".concat(
      Array.from({ length: addressLength })
        .map(() => possibleCharacters[generateRandomNumber(selectionLength)])
        .join("")
    );

    return {
      bitcoinAddress: generatedAddress,
      bitcoinBalance: 100 + +(Math.random() * 100).toFixed(2),
    };
  };

  return {
    generateBitcoinAddress,
  };
})();

const users = [
  {
    email: "test1@example.com",
    password: "1234",
    bitcoinAddress: "1MsYFA2HyCiTQ1X2vPByirQo3i7HQ9yNvb",
    bitcoinBalance: 174.13,
  },

  {
    email: "tamara26@yahoo.com",
    password: "tamara",
    bitcoinAddress: "1c9y8xHAGc1CjFfX3eW5V85M9sJax6o",
    bitcoinBalance: 361.54,
  },

  {
    email: "antone87@gmail.com",
    password: "antone",
    bitcoinAddress: "1cKP3SVjSFwbGDYwJgeqfB4gYMEw",
    bitcoinBalance: 153.24,
  },
];

export const db = (() => { // db.getUsers
  const getUsers = () =>
  // map을 실행해서 users 정보들을 객체화 시킴
  // 비밀번호와 나머지들 중 나머지만 불러온다는 뜻
    delayedResolve(users.map(({ password, ...rest }) => rest));

  const addUser = (email, password) => {
    const foundUser = users.find((user) => user.email === email);

    if (foundUser) {
      throw new Error("Email already exists.");
    }

    const newUser = {
      email,
      password,
      ...bitcoinAddressBuilder.generateBitcoinAddress(),
    };

    users.push(newUser);

    return delayedResolve(newUser);
  };

  const findUser = (email, password) => {
    const foundUser = users.find((user) => user.email === email);

    if (!foundUser) {
      throw new Error("User not found");
    }

    if (foundUser.password !== password) {
      throw new Error("Password not matched.");
    }

    return delayedResolve(foundUser);
  };

  return {
    getUsers,
    addUser,
    findUser,
  };
})();

```

### 유저 등록하기  

```jsx
// BitcoinApp.js  
import React, { useState, useEffect } from "react";
import * as authAPI from "../service/auth";
import styled from "styled-components";
import UserDetail from "./UserDetail";
// RegisterForm을 불러옴
import RegisterForm from './RegisterForm'

// RegisterForm을 이용해 유저 정보를 가져와 화면을 업데이트하세요.
const WrappedUserDetail = styled(UserDetail)`
  & + & {
    margin-top: 12px;
  }
`;

export default function BitcoinApp() {
  const [users, setUsers] = useState(undefined);
  
  const handleSubmit = (formData) => {
    authAPI
    // db.addUser 실행 : 중복이 되어 있지 않으면 newUser 객체 만들어서 기존 유저에 push
        .registerUser(formData)
    // 성공하면 getUsers를 실행해서 map으로 필요한 정보만 뽑아오고
        .then(authAPI.getUsers)
    // users 상태 변경
        .then(setUsers)
    // 에러는 따로 잡음  
        .catch(console.error)
  }

  useEffect(() => {
    authAPI.getUsers().then((data) => {
      console.log(data);
      setUsers(data);
    });
  }, []);

  if (!users) {
    return <div>유저 정보를 불러오는 중입니다...</div>;
  }

  return (
    <div>
         // RegisterForm을 불러오고, props로 onSubmit을 넘겨줌
        <RegisterForm onSubmit={handleSubmit}/>
      {users.map((user) => (
        <WrappedUserDetail {...user} />
      ))}
    </div>
  );
}

// RegisterForm.jsx  
import React, { useRef } from "react";
import styled from "styled-components";

export default function RegisterForm({ className, onSubmit }) {
  const formRef = useRef();
  const emailRef = useRef();
  const passwordRef = useRef();
  const confirmPasswordRef = useRef();

  const submitForm = (e) => {
    e.preventDefault();
// 받아온 값을 저장함
    const email = emailRef.current.value;
    const password = passwordRef.current.value;
    const confirmPassword = confirmPasswordRef.current.value;
// 받아온 값의 문자 길이, 패스워드 동일 입력 여부를 확인함
    if (email.length === 0 || password.length === 0) {
      return;
    }

    if (confirmPassword !== password) {
      confirmPasswordRef.current.setCustomValidity("Different from password");
      return;
    }

    const formData = {
      email,
      password,
    };
// 또한 제출버튼 클릭시 props로 받아온 onSUbmit함수에 formData를 매개변수로 전달하여 실행
// formRef를 리셋함
    onSubmit(formData);
    formRef.current.reset();
  };

  return (
      // form 형식으로 email. password, confirmpassword를 받음
    <Container className={className}>
      <form ref={formRef}>
        <fieldset>
          <label htmlFor="email">Email</label>
          <input
            placeholder="Enter email."
            required
            ref={emailRef}
            id="email"
            type="email"
            name="email"
            autocomplete="off"
          />
        </fieldset>

        <fieldset>
          <label htmlFor="password">Password</label>
          <input
            required
            ref={passwordRef}
            id="password"
            type="password"
            name="password"
            placeholder="Enter password."
          />
        </fieldset>

        <fieldset>
          <label htmlFor="confirmPassword">Confirm Password</label>
          <input
            required
            ref={confirmPasswordRef}
            id="confirmPassword"
            type="password"
            name="confirmPassword"
            placeholder="Enter password again."
          />
        </fieldset>
        <RegisterButton onClick={submitForm}>Register</RegisterButton>
      </form>
    </Container>
  );
}

const Container = styled.div`
  fieldset {
    margin: 0;
    box-sizing: border-box;
    width: 100%;
  }

  label {
    margin-right: 4px;
  }

  input[type="password"]:invalid,
  input[type="email"]:invalid {
    border: 1px solid red;
  }

  input[type="password"]:valid,
  input[type="email"]:valid {
    border: 1px solid green;
  }

  form:invalid {
    border: 5px solid #ffdddd;
  }
`;

const RegisterButton = styled.button.attrs({ type: "submit" })`
  width: 100%;
  height: 40px;
`;


// App.js  
import React from 'react';
import "./App.css";
import BitcoinApp from "./BitcoinApp/BitcoinApp";
import styled from "styled-components";

const Container = styled.div`
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
`;

function App() {
  return (
    <Container>
      <BitcoinApp />
    </Container>
  );
}

export default App;

```

### 등록 페이지, 유저 목록 페이지 추가하기

```jsx
// App.js  
import React from 'react';
import "./App.css";
import BitcoinApp from "./BitcoinApp/BitcoinApp";
import styled from "styled-components";

const Container = styled.div`
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
`;

function App() {
  return (
    <Container>
          // BitcoinApp 컴포넌트를 불러옴  
      <BitcoinApp />
    </Container>
  );
}

export default App;

// auth.js
import { db } from "./db";

export const getUsers = () => db.getUsers();

export const loginUser = ({ email, password }) => db.findUser(email, password);

export const registerUser = ({ email, password }) =>
  db.addUser(email, password);
// db.js  
const delayedResolve = (data) =>
  new Promise((resolve, reject) => setTimeout(() => resolve(data), 250));

const bitcoinAddressBuilder = (() => {
  const possibleCharacters =
    "1234567890ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz";

  const generateRandomNumber = (max, min = 0) =>
    Math.floor(Math.random() * (max - min + 1)) + min;

  // P2PKH invoice address format
  const generateBitcoinAddress = () => {
    const selectionLength = possibleCharacters.length - 1;
    const addressLength = generateRandomNumber(34, 25);

    const generatedAddress = "1".concat(
      Array.from({ length: addressLength })
        .map(() => possibleCharacters[generateRandomNumber(selectionLength)])
        .join("")
    );

    return {
      bitcoinAddress: generatedAddress,
      bitcoinBalance: 100 + +(Math.random() * 100).toFixed(2),
    };
  };

  return {
    generateBitcoinAddress,
  };
})();

const users = [
  {
    email: "test1@example.com",
    password: "1234",
    bitcoinAddress: "1MsYFA2HyCiTQ1X2vPByirQo3i7HQ9yNvb",
    bitcoinBalance: 174.13,
  },

  {
    email: "tamara26@yahoo.com",
    password: "tamara",
    bitcoinAddress: "1c9y8xHAGc1CjFfX3eW5V85M9sJax6o",
    bitcoinBalance: 361.54,
  },

  {
    email: "antone87@gmail.com",
    password: "antone",
    bitcoinAddress: "1cKP3SVjSFwbGDYwJgeqfB4gYMEw",
    bitcoinBalance: 153.24,
  },
];

export const db = (() => {
  const getUsers = () =>
    delayedResolve(users.map(({ password, ...rest }) => rest));

  const addUser = (email, password) => {
    const foundUser = users.find((user) => user.email === email);

    if (foundUser) {
      throw new Error("Email already exists.");
    }

    const newUser = {
      email,
      password,
      ...bitcoinAddressBuilder.generateBitcoinAddress(),
    };

    users.push(newUser);

    return delayedResolve(newUser);
  };

  const findUser = (email, password) => {
    const foundUser = users.find((user) => user.email === email);

    if (!foundUser) {
      throw new Error("User not found");
    }

    if (foundUser.password !== password) {
      throw new Error("Password not matched.");
    }

    return delayedResolve(foundUser);
  };

  return {
    getUsers,
    addUser,
    findUser,
  };
})();

// BitcoinApp.jsx
import React from "react";
import { Redirect, BrowserRouter, Switch, Route } from "react-router-dom";
import UsersPage from "./pages/UsersPage";
import RegisterPage from "./pages/RegisterPage";

export default function BitcoinApp() {
  return (
      // 브라우저 라우터
    <BrowserRouter>
          // 스위치 통해서 해당 페이지로 이동하게 함
      <Switch>
          // "/"
        <Redirect exact from="/" to="/users" />
        // "/users"는 Userspage로 이동
          <Route path="/users" component={UsersPage} />
       // "/register"는 RegisterPage로 이동
        <Route path="/register" component={RegisterPage} />
      </Switch>
    </BrowserRouter>
  );
}
// 방법 2
import {Redirect, Route} from 'react-router-dom'
return (
	<Route>
		<Redirect to={{
                  pathname: '/login',
                  state: {from: props.loginState}
		}}/>
	</Route>
      )

// Userpage.jsx  
import { useState, useEffect } from "react";
import styled from "styled-components";
import { Link } from "react-router-dom";
import { PageLayout } from "../PageLayout";
import UserDetail from "../components/UserDetail";
import * as authAPI from "../../service/auth"

function UsersPage() {
  const [users, setUsers] = useState(undefined);
  
  // authAPI.getUsers를 이용해 유저 목록을 불러오세요.
  useEffect(() => {
    authAPI
        .getUsers()
        .then(setUsers)
        .catch(console.error)
  }, [])

  return (
    <PageLayout>
      <nav>
        <Link to="/register">Register</Link>
      </nav>

      {!users ? (
        <div>유저 정보를 불러오는 중입니다...</div>
      ) : (
        users.map((user) => <WrappedUserDetail {...user} />)
      )}
    </PageLayout>
  );
}

export default UsersPage;

const WrappedUserDetail = styled(UserDetail)`
  & + & {
    margin-top: 12px;
  }
`;

// RegisterPage.jsx
import { Link, useHistory } from "react-router-dom";
import styled from "styled-components";
import { PageLayout } from "../PageLayout";
import RegisterForm from "../components/RegisterForm";
import * as authAPI from "../../service/auth"

export default function RegisterPage() {
  const history = useHistory();

  const handleSubmit = (formData) => {
    // formData에는 email, password가 들어있습니다.
    // 이 정보를 바탕으로 authAPI.registerUser 를 이용해 유저를 등록하세요.
    // 성공적으로 유저를 등록했으면 유저 목록 페이지로 이동하세요.
    console.log(formData)
    
    authAPI
        .registerUser(formData)
      // 해당 URL로 이동하게 함
        .then(() => history.push('/users'))
        .catch(console.error)
  };

  return (
    <PageLayout>
      <nav>
        <Link to="/users">Users</Link>
      </nav>
      <WrappedRegisterForm onSubmit={handleSubmit} />
    </PageLayout>
  );
}

const WrappedRegisterForm = styled(RegisterForm)`
  margin-bottom: 12px;
`;


// registerForm.jsx  
import React, { useRef } from "react";
import styled from "styled-components";

export default function RegisterForm({ className, onSubmit }) {
  const formRef = useRef();
  const emailRef = useRef();
  const passwordRef = useRef();
  const confirmPasswordRef = useRef();

  const submitForm = (e) => {
    e.preventDefault();

    const email = emailRef.current.value;
    const password = passwordRef.current.value;
    const confirmPassword = confirmPasswordRef.current.value;

    if (email.length === 0 || password.length === 0) {
      return;
    }

    if (confirmPassword !== password) {
      confirmPasswordRef.current.setCustomValidity("Different from password");
      return;
    }

    const formData = {
      email,
      password,
    };

    onSubmit(formData);
    formRef.current.reset();
  };

  return (
    <Container className={className}>
      <form ref={formRef}>
        <fieldset>
          <label htmlFor="email">Email</label>
          <input
            placeholder="Enter email."
            required
            ref={emailRef}
            id="email"
            type="email"
            name="email"
            autocomplete="off"
          />
        </fieldset>

        <fieldset>
          <label htmlFor="password">Password</label>
          <input
            required
            ref={passwordRef}
            id="password"
            type="password"
            name="password"
            placeholder="Enter password."
          />
        </fieldset>

        <fieldset>
          <label htmlFor="confirmPassword">Confirm Password</label>
          <input
            required
            ref={confirmPasswordRef}
            id="confirmPassword"
            type="password"
            name="confirmPassword"
            placeholder="Enter password again."
          />
        </fieldset>
        <RegisterButton onClick={submitForm}>Register</RegisterButton>
      </form>
    </Container>
  );
}

const Container = styled.div`
  fieldset {
    margin: 0;
    box-sizing: border-box;
    width: 100%;
  }

  label {
    margin-right: 4px;
  }

  input[type="password"]:invalid,
  input[type="email"]:invalid {
    border: 1px solid red;
  }

  input[type="password"]:valid,
  input[type="email"]:valid {
    border: 1px solid green;
  }

  form:invalid {
    border: 5px solid #ffdddd;
  }
`;

const RegisterButton = styled.button.attrs({ type: "submit" })`
  width: 100%;
  height: 40px;
`;


```

### 상세 페이지 추가하기

```jsx
// registerForm.jsx  
import { Link, useHistory } from "react-router-dom";
import styled from "styled-components";
import * as authAPI from "../../service/auth";
import { PageLayout } from "../components/PageLayout";
import RegisterForm from "../components/RegisterForm";
import Navigation from "../components/Navigation";

export default function RegisterPage() {
  const history = useHistory()

  const handleSubmit = (formData) => {
    // formData에는 email, password가 들어있습니다.
    // 이 정보를 바탕으로 authAPI.registerUser 를 이용해 유저를 등록하세요.
    // 성공적으로 유저를 등록했으면 유저 목록 페이지로 이동하세요.
    console.log(formData)
    const handleSubmit = (formData) => {
    authAPI
        .registerUser(formData)
        .then(() => history.push('/users'))
  };
}
  return (
    <PageLayout>
      <Navigation>
        <Link to="/users">유저 목록</Link>
      </Navigation>
      <h2>유저 회원가입</h2>
      <WrappedRegisterForm onSubmit={handleSubmit} />
    </PageLayout>
  );
}

const WrappedRegisterForm = styled(RegisterForm)`
  margin-bottom: 12px;
`;


// userDetailPage.jsx
import React, { useState, useEffect } from "react";
import { Link, useHistory, useParams } from "react-router-dom";
import * as authAPI from "../../service/auth";
import { PageLayout } from "../components/PageLayout";
import TransferForm from "../components/TransferForm";
import Navigation from "../components/Navigation";
import { colors } from "../../style/colors";
import styled from "styled-components";
import { Bitcoin } from "../elements/Bitcoin";

function UserDetailPage() {
  const { email } = useParams();
  const [addresses, setAddresses] = useState([]);
  const history = useHistory();
  const [user, setUser] = useState(null);
  const [error, setError] = useState("");
  
  // 유저의 상세 정보를 로드하여 user에 저장하고, 정보를 보여주세요.
  useEffect(() => {
    const decodedEmail = decodeURIComponent(email)
    
    authAPI
        .getUser(decodedEmail)
        .then(setUser)
        .catch(e => setError(e.message))
    authAPI
        .getUsers()
        .then(users => users.map(user => user.bitcoinAddress))
        .then(setAddresses)
        .catch(e => setError(e.message))
  }, [])

  const handleSubmit = (formData) => {
    const { address, amount } = formData;
    // address는 다른 유저의 주소입니다.
    // 비트코인을 다른 유저에게 전송하는 기능을 구현하세요.
    // 성공적으로 전송했으면 유저 목록 페이지로 이동하세요.
    console.log(address, amount)
    
    authAPI
        .transferBitcoin(user.bitcoinAddress, address, amount)
        .then(() => history.push('/users'))
        .catch(e => setError(e.message))
  };

  return (
    <PageLayout>
      <Navigation>
        <Link to="/users">유저 목록</Link>
      </Navigation>

      <h2>유저 상세정보</h2>

      {!user ? (
        <div>Loading...</div>
      ) : (
        <>
          <Bitcoin>
            <div>
              <strong className="title">Bitcoin Address</strong>
              <span className="content">{user.bitcoinAddress}</span>
            </div>

            <div>
              <strong className="title">Bitcoin Balance</strong>
              <span className="content">{user.bitcoinBalance} BTC</span>
            </div>
          </Bitcoin>

          <h3>비트코인 전송</h3>

          <TransferForm addresses={addresses} onSubmit={handleSubmit} />
          {error && <div>{error}</div>}
        </>
      )}
    </PageLayout>
  );
}

export default UserDetailPage;

```

### useState를 활용하여 User Table 상태관리 앱 만들기

```jsx
import React, { Fragment, useState, useEffect } from "react";
import styled from "styled-components";
import axios from "axios";
import UserTable from "./UserTable";

const checkboxes = [
  {
    id: "filter-username",
    name: "filter-username",
    pathFn: (user) => user.username,
    label: "Filter by Username",
  },

  {
    id: "filter-city",
    name: "filter-city",
    pathFn: (user) => user.address.city,
    label: "Filter by City",
  },

  {
    id: "filter-company",
    name: "filter-company",
    pathFn: (user) => user.company.name,
    label: "Filter by Company",
  },
];

export default function App() {
  // 데이터를 필터링 하는 코드를 구현해보세요.
  // searchData - search에 기반이 되는 리스트입니다.
  // 쿼리를 안 쳤을 때 보여주는 초기 데이터  
  const [searchData, setSearchData] = useState([])
  // users - query를 기준으로 search하여 결과를 저장하는 리스트입니다.
  const [users, setUsers] = useState([]);
  // query - 유저의 입력입니다.
  const [query, setQuery ] = useState('')
  // filters - filter name에 따른 pathFn을 저장하는 맵입니다.
  const [filters, setFilters] = useState({})
  
  const handleCheckboxChange = (pathFn) => (e) => {
    const name = e.target.name
    if (e.target.checked) {
        // filter를 추가합니다.
        return setFilters(filterObj => ({ ...filterObj, [name]: pathFn }))
    }
    
    // filter를 제거합니다.
    setFilters(({ [name] : _, ...rest }) => rest)
  }

  useEffect(() => {
    axios
      .get("https://jsonplaceholder.typicode.com/users")
      .then((res) => {
        const fetchedUsers = res.data
        setUsers(fetchedUsers)
        setSearchData(fetchedUsers)
      })
  }, []);
  
  useEffect(() => {
    // query가 바뀔 때 서치 로직을 구현하세요.
    // 쿼리의 변경을 감지
    console.log('쿼리가 바뀌었습니다.', query)
    if (!query) {
        return setUsers(searchData)
    }
    // filters 
    // {
    //   ['filter-username'] : pathFn
    //   ['filter-city'] : pathFn
    // }
    
    // user => user.username
    // pathFn(user) "Karianne"
    // ["Karianne", "City", "Address"]
    // ["kariannecityaddress", search(query) !== -1 ex) "kar"]
    const stringifyUser = (user) => {
        return Object
            .values(filters)
            .map(fn => fn(user))
            .map(str => str.toLowerCase())
            .join()
    }
    
    const isUserQualified = (user) => {
        stringifyUser(user)
        .search(query) !== -1
    }
    
    const filteredUsers = searchData.filter(isUserQualified)
        setUsers(filteredUsers)
  }, [query, searchData])

  return (
    <Container>
      <div>
        <label htmlFor="search-query">Search</label>
        <input
          id="search-query"
          type="text"
          name="search-query"
          value={query}
          onChange={(e) => setQuery(e.target.value.trim().toLowerCase())}
        />
        <button type="button" onClick={() => {
            setQuery('')
            setFilters({})
        }} >
          Reset
        </button>
      </div>

      <CheckboxController>
        {checkboxes.map(({ id, name, pathFn, label }) => (
          <Fragment key={id}>
            <input
              type="checkbox"
              id={id}
              name={name}
              onChange={handleCheckboxChange(pathFn)}
            />
            <label htmlFor={id}>{label}</label>
          </Fragment>
        ))}
      </CheckboxController>

      <UserTable users={users} />
    </Container>
  );
}

const Container = styled.div`
  min-height: 600px;
`;

const CheckboxController = styled.div`
  padding: 8px 0;

  input:not(:first-of-type) {
    margin-left: 20px;
  }
`;

```

### API 이용해 카페메뉴 불러오기

```jsx
import React, {useState} from 'react';
import axios from "axios";

// 지시사항에 따라 출력 결과와 동일한 동작을 하는 코드를 작성하세요.
function App() {
  
  const [data, setData] = useState("")
  
  const handleOnclick = () => {
    async function main(){
        const API_url = `https://${window.location.hostname}:8190/data`
        // axios.get(url) : API를 요청할때 사용
        const response = await axios.get(API_url)
        setData(response.data)
    }
    main()
  }


  return (
    <div className="App">
        {data === "" ? 
        "":(
            data.map((datas) => (
                <li>{datas.item}</li>
            ))
           )
        }
        <button id="load" onClick={handleOnclick}>불러오기</button>
    </div>
  );
}

export default App;

```

# Styled component  

## **CSS Module**  

```css
class.id 등에 random string을 달아주기 때문에 
선택자가 겹칠 우려가 없음  

스타일 충돌을 방지하고 코드를 격리하여 채계적으로 CSS 설계가 가능  

스타일링 직접 하나하나 해야 함  
```

```jsx
// App.jsx
import styles from "./app.module.css";

export default function App() {
    return (
    	<div>
            // css의 .title을 가져옴
        	<h1 className={styles.title}>Pink Hello World</h1>
            // 일반 string title
            <div className={styles.['buttons-container']} />
            <h1 className={"title"}>Normal Hello World</h1>
        </div>
    )
}

// app.module.css  
h1 {
    font-size: 1.5rem;
}

.title {
    font-size: 2.5rem;
    color: palevioletred;
}
```

## UI framework  

```css
이미 다 만들어져 있어서 간편하고 쉽게 쓰기에 좋음  
styling의 학습 및 훈련이 필요한 초심자들에게는 비추천  
해당 framework의 디자인철학을 벗어나기 쉽지 않음  
컴포넌트들을 커스터마이징 하기 어려움
```

```jsx
// App.jsx  (Ant Design 예시)
import "antd/dist/antd.css";
import { Button } from "antd";

export default function App(){
    return{
        <div>
        	<Button type = "primary">Primary Button</Button>
            <Button type = "secondary">Secondary Button</Button>
            <Button type = "danger">Danger Button</Button>
        </div>
    }
}
```

## CSS framework  

```css
거대한 CSS 파일 하나를 가져오는 것임  
개발자가 따로 CSS 파일을 작성하지 않아도  
HTML에 클래스만 적어주면 정해진 규칙대로 스타일링이 적용됨  
CSS에 대한 이해력이 있어도 해당 framework를 사용하기 위한 학습을 또다시 해야함  
이미 다 만들어져 있어서 styling의 학습 및 훈련이 필요한 초심자들에게는 비추천
```

```jsx
// App.jsx (W3CSS 예시)
import { Helmet } from "react-helmet";

export default function App(){
    return(
    	<div>
        	<Helmet>
            	<link 
                    rel = "stylesheet"
                    href = "https://www.w3schools.com
                            					/w3css/4/w3.css" 
                    />
            </Helmet>
            <div className = "w3-container w3-green">
            	<h1>W3Schools Demo</h1>
            	<p>Resize this responsive page</p>
            </div>
            <div className="w3-row-padding">
            	<div className="w3-third">
                	<h2>London</h2>
                    <p>Lorem</p>
                    <p>Lorem</p>
                </div>
            </div>
        </div>
    )
}
```

## CSS-in-JS library  

```css
따로 CSS 파일을 만들 것 없이 JSX 파일 안에서 스타일링까지 해결 가능함  
컴포넌트 재사용성이 쉬워짐  
JS 값들을 Props로 넘겨줘서 해당 JS 값에 의도된 styling을 바로 적용할 수 있음  
class 이름에 random string이 생성되기 때문에 선택자 이름이 겹칠 우려가 없음  
스타일링을 직접 개발자가 하나하나 해야함
```

```jsx
import styled from "styled-components";

const Title = styled.h1`
	font-size: 1.5rem;
	text-align: center;
	color: palevioletred;
`

export default function App(){
    return <Title>Hello World</Title>
}
```

## SCSS  

```scss
/* SCSS를 이용해 코드를 리팩토링하세요, */
.container {
    padding: 10px;
    background-color: lightgray;
    display: flex;
    flex-direction: column;
    align-items: center;
    .counter {
        width: 100px;
        height: 50px;
        line-height: 50px;
        font-size: 2rem;
        border: 1px solid black;
        border-radius: 8px;
        text-align: center;
    }
    .buttons-container {
    margin-top: 20px;
    }
    
    button {
    color: white;
    width: 80px;
    height: 50px;
    text-align: center;
    border-radius: 10px;
        + button {
            margin-left: 10px;
        }
        
        &.inc{
        background-color: blue;       
        }
        &.dec{
        background-color: red;
        }
        &:hover{
            box-shadow: 10px 5px 5px gray;
        }
    }

}
```

![image-20210812003939039](C:\Users\joo\AppData\Roaming\Typora\typora-user-images\image-20210812003939039.png)

## javaScript template literal 

```js
Template literals: 템플릿 리터럴은 내장된 표현식을 허용
쉽게 말해 문자열 안에서 js 표현식을 사용할 수 있게 하는 문법

`string text ${expression} string text`

const boolean = true  
const message = `hello ${boolean}`

console.log(message)

---
const name = "chalie"
const gender = "male"
const message = `hello ${gender === "male" ? "Mr." : "Mrs." ${name}, nece to meet you`

```

```js
const isAdult = (n) => n > 19;
const name = "mike"

const answer = `My name is ${name}, and I am ${isAdult(35) ? "an adult" : "a child"}`
```

## styled components  

```jsx
const Button = styled.button`
	font-size: 1em;
	margin: 1em;
	padding: 0.25em 1em;
	border: 2px solid palevioletred;
	border-radius: 3px;
	background: ${props => props.primary ? "palevioletred" : "white"};
	color: ${props => props.primary ? "white" : "palevioletred"};`

function App(){
	return(
		<div>
        	<Button>Normal Button</Button>
            <Button primary>Primary Button</Button>
        </div>
	)
}
`
```

### react-css 예제

```jsx
API Response와 과목, 트랙 리스트 UI 연동하기

import axios from "axios";
import { useState, useEffect } from "react";
import styled from "styled-components";
import Tab from "./Tab.jsx";
import SearchTextField from "./SearchTextField.jsx";
import CardCount from "./CardCount.jsx";
import TrackCard from "./TrackCard.jsx";
import CourseCard from "./CourseCard.jsx";
import Pagination from "./Pagination.jsx";

const Container = styled.div`
  display: flex;
  align-items: center;
  height: 100vh;
  width: 1232px;
  margin: auto;
  padding-top: 100px;
  flex-direction: column;
`;


const TracksContainer = styled.div`
  display: grid;
  grid-template-columns: repeat(3, 398px);
  grid-column-gap: 19px;
  grid-row-gap: 32px;
`;

const CoursesContainer = styled.div`
  display: grid;
  grid-template-columns: repeat(4, 296px);
  grid-column-gap: 16px;
  grid-row-gap: 24px;
`;

export default function App() {
  const [currTab, setCurrTab] = useState("트랙");
  const [searchValue, setSearchValue] = useState("");
  const [currPage, setCurrPage] = useState(0);
  const [cardData, setCardData] = useState([]);
  const [totalCardCount, setTotalCardCount] = useState(0);

  const handleClickTab = (tab) => {
    if (tab !== currTab) setSearchValue("");
    setCurrTab(tab);
  };

  const handleChangeSearch = (val) => {
    setSearchValue(val);
  };
  
  useEffect(() => {
    //여기에서 과목, 트랙 데이터를 서버로부터 가져오는 API를 호출하세요.
    (async function main(){
        if (currTab==="트랙"){        
            const API_END_POINT = "https://api-beta.elicer.io:6664/org/academy/"
            const trackUrl = `${API_END_POINT}track/list/?offset=0&count=6`;
            const response = await axios.get(trackUrl);

            setTotalCardCount(response.data.track_count);
            setCardData(response.data.tracks);
        }
        if (currTab==="과목"){        
            const API_END_POINT = "https://api-beta.elicer.io:6664/org/academy/"
            const courseUrl = `${API_END_POINT}course/list/?offset=0&count=8`;
            const response = await axios.get(courseUrl);

            setTotalCardCount(response.data.course_count);
            setCardData(response.data.courses);
        }
    })()

  }, [currTab]);

  return (
    <Container>
      <Tab currTab={currTab} onClick={handleClickTab} />
      <SearchTextField value={searchValue} onChange={handleChangeSearch} />
      <CardCount count={totalCardCount}/>
      {currTab === "트랙" ? (
        <TracksContainer>
          {cardData.map((_, i) => (
            <TrackCard
              key={`track-card-${i}`}
            />
          ))}
        </TracksContainer>
      ) : (
        <CoursesContainer>
          {cardData.map((course, i) => (
            <CourseCard
              title={course.title}
              key={`course-card-${i}`}
            />
          ))}
        </CoursesContainer>
      )}
      <Pagination
        currPage={currPage}
        pageCount={15}
        onClickPage={setCurrPage}
      />
    </Container>
  );
}


```

# React 앱 배포

```python
# yarn start
개발용 코드

http 배포시 80 포트로 배포
https 는 443
nginx 사용 하지말기 


실제 배포시에는 yarn start는 사용하지 않아도 되고, yarn build 명령어를 통해 컴파일한 static html/js/css 파일을 사용하게 됩니다.
따라서 flask 서버 포트만 사용하게 되고 서버 외에 다른 것은 띄우지 않아도 됩니다.
nginx 설정을 하시면 별도 flask 서버 코드 수정 없이도 사용할 수 있습니다.
예를들어 다음과 같이 초기 페이지를 설정해주면 됩니다.
location / {
    root   html;
    index  index.html index.htm;
}
proxy pass는 http://localhost/:<서버 포트> 로 설정해주시면 됩니다.
https://ichi.pro/ko/react-flask-aeb-bildeu-mich-baepo-78789469870041
nginx를 사용하지 않고 한다면 아래 내용을 참고하시면 됩니다.
https://ichi.pro/ko/react-flask-aeb-bildeu-mich-baepo-78789469870041
    
팁 : 실행스크립트를 만든다.
로컬호스트는 사용하지 말기 (서버 IP를 environment로 가져오기)
서버 실행할때 IP 주소를 가져와서 실행


# yarn build
프로젝트 완성한 후 비쥬얼스튜디오 코드에서 yarn build 통해서 빌드해주어야 함 (모든 소스를 최대한 모아서 오로지 보여주기 위한 요소들만 저장시켜 줌) #서버 터미널에서 실행

링크 : https://chiseled-browser-c2e.notion.site/React-Flask-Azure-c3bb1ee37c02413eae98c88e6f2ab617

azure 로그인  

리소스 만들기 클릭  

Ubuntu Server 클릭  
	구독 선택  
    가상머신 이름 마음대로  
    관리자 계정 : 사용 아이디 입력  
    인바운트 포트 규칙  (HTTP, HTTPS, SSH 선택)
    
프라이빗 키 다운로드 및 리소스 만들기해서 다운 받기
**잃어버리면 안되고 잘 보관해두기**  

다시 최신리소스로 돌아가서 확인  

왼쪽 메뉴에서 연결 탭 클릭  

ssh ~~~ key ip가 있음  
파워셸들어가서 위의 명령어 입력  
	->> azure 터미널로 이동  

터미널 내에서 배포할 프로젝트를 git clone로 받아옴  
	서버컴으로 클론
    
해당 경로로 이동해서 ls 사용해서 파일 확인  

npm install  

npm start 

sudo apt update  

sudo apt install npm -y

** npm install 꼭 해줘야 함

npm run build  

npm -v 로 버전 확인  

cd build  
# build 경로 기억해두기 이 값을 추후에 default 값으로 설정
pwd	

sudo apt update
sudo apt upgrade -y

sudo apt install nginx -y
cd /etc/nginx/sites-available

ls 시 default 값이 있어야 함  

> cd /etc/nginx/sites-available
> sudo chmod 777 default
> vi default

- 기본값인 root /var/www/html; 부분을 아까 기억해둔 build 폴더 경로로 변경

           - vi 입력 명령어 : 화살표로 입력할 곳으로 간 후 ⇒ i 키보드 입력 ⇒  내용 작성 ⇒ Esc 키도브 입력

           - vi 저장 명령어 : Esc 키보드 입력 ⇒ wq! ⇒ 엔터
                
# 쓰기 모드로 변경 법 : sudo chmod 777 default
저장 : wq 
나가기 : q

sudo service nginx start
sudo service nginx restart로 다시 켜줌  


Azure VM에 나와있는 공용 IP 주소 확인
해당 경로 접속 # 여기까지가 프론트엔드만 킨 거임  

# 플라스크 서버를 켜야함  
vi default  
default 파일 내려가다 보면  
location/ 부분으르 수정해야 함

# 요청이 있을 경우 내가 사용하는 포트로 데이터를 넘겨주겠다.
location / api {
    # 세미콜론 필수  
    proxy_pass http://localhost:5000; 
}

sudo service nginx restart  

cd ~/covid-map/  

ls  

# app.py 실행  
sudo apt install python3-pip  
# requirements.txt (따로 만들어줘야 함)
pip install -r reqirements.txt (tab 눌러 자동완성)  

python3 app.py  

# 실행 서버를 확인 해보기  

# 우리가 발급받은 api 경로로 바꿔줘야함  

# vi app.py  
# 불러오는 부분을 "api/covidData"로 바꿔줘야 함
# 바꾸기 전에 nginx 끄기
프론트엔드 부분의 env.js 를 
우리가 발급받은 주소로 바꿔야함

src/env.js
export const BACKEND_URL = "http://{공용IP주소}/api"
# 이렇게 파이썬 플라스크 포트로 넘어감  

# 서버 부분 바뀌면 다시 빌드
npm run build

# ngnx 켜기, and  
python3 app.py  


```



```js
1. 엘리스 가상머신 접속

ssh elice@[YOUR_DNS_NAME] 입력후 yes, 비밀번호 입력  

2. 필요한 라이브러리 설치  
> sudo apt update
> sudo apt install npm -y
> sudo apt install python3-pip -y
// sudo apt install nginx -y

3. 배포할 프로젝트 git clone
// 클론 전에 모든 파일을 올려야 진행이 될 듯  

4. 클론한 프로젝트 경로 이동
cd KIMHANBIN
cd frontend
npm run build
ls
// build 폴더 위치 적기 : /home/elice/hanbinproject/KimHanBin-dev/frontend/build	
5. ngnix 기본 설정 파일 재설정
// sudo apt update
// sudo apt upgrade -y
// sudo apt install nginx -y
cd /etc/nginx/sites-available

ls 시 default 값이 있어야 함  

> cd /etc/nginx/sites-available
> sudo chmod 777 default
> vi default

- 기본값인 root /var/www/html; 부분을 아까 기억해둔 build 폴더 경로로 변경
// ex : root /home/azureuser/covid-map/build;

> sudo service nginx restart

6. 공용 IP 주소로 접속
DNS : elice@kdt-1st-project-60.koreacentral.cloudapp.azure.com
공용 ip : 52.231.66.21

종료 : 184342
```

