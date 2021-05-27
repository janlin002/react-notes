<h3>useReduer</h3>

useState 的替代方案。它接收一个形如 (state, action) => newState 的 reducer，并返回当前的 state 以及与其配套的 dispatch 方法。

```bash
const [state, dispatch] = useReducer(reducer, 預設值);
```

```bash
import React,{useReducer} from 'react';

const App = () =>{
   const initialState = { count: 0 };//初始值
   
   //條件式
  const reducer = (state,action)=>{
    switch(action.type){
      case 'increment':
      return {count:state.count+1};
      case 'decrement':
      return {count:state.count-1};
      default:
        throw new Error()
    }
  }
  //畫面
  const [state,dispatch] = useReducer(reducer,initialState);
  return(
    <div>
      <reducer>{state.count}</reducer>
      <button onClick={()=>dispatch({type:'increment'})}>+</button>
      <button onClick={()=>dispatch({type:'decrement'})}>-</button>
    </div>
  )
}
export default App
```
