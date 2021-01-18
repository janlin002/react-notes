<h1>Hook</h1>
<h3>Hook 是 React 16.8 中增加的新功能。它讓你不必寫 class 就能使用 state 以及其他 React 的功能。</h3>

<h3>影音資源</h3>

[技術胖](https://www.bilibili.com/video/BV1y4411Q7yH?from=search&seid=15129246938121288056)

[合一大師](https://www.bilibili.com/video/BV1ca4y1Y7R1?p=3)

[老菜鳥](https://www.bilibili.com/video/BV1VE411w7wi?from=search&seid=15129246938121288056)

<h3>那...為什麼要Hook?</h3>

[技術文章](https://www.mdeditor.tw/pl/pG7r/zh-tw)

<h3>Hook簡介</h3>
Hook 是 JavaScript function<br>

1.只在 最上層 呼叫 Hook。不要在迴圈、判斷式、或是嵌套 function 中呼叫 Hook。<br>
2.只在 React function component 呼叫 Hook。不要在一般 JavaScript function 中呼叫 Hook。

<h3>State Hook</h3>

function 中的 [useState] 如同 class 中的 [this.state];<br>

```bash
const [count, SetCount] = useState(0);
=> 
const [目前state的值,可以更新state的function] = useState(回傳的值)
```

[官網](https://zh-hant.reactjs.org/docs/hooks-state.html)

<h3>Effect Hook</h3>

將在每次 render() 後，執行!

```bash
  useEffect(()=>{
      //組件掛載
    return()=>{
      //組件卸載
    }
  })
```

<h3>用useEffect取代生命週期</h3>

```bash
useEffect() = componentDidMount + componentDidUpdate + componentWillUnmount
```

<h4>無需清除的 Effect</h4>

```bash
=> componentDidMount + componentDidUpdate
```

用意：有時候，我們希望在 React 更新 DOM 之後執行一些額外的程式碼。

<h4>需清除的 Effect</h4>

```bash
=> componentDidMount + componentDidUpdate + componentWillUnmount
```

用意：我們可能想要設定對某些外部資料來源的 [subscription]。在這種情況下，請務必進行清除，以免造成 memory leak！

[官網](https://zh-hant.reactjs.org/docs/hooks-effect.html)

<h3>Hook規則</h3>
<h5>只在最上層呼叫 Hook</h5>
<h5>只在 React Function 中呼叫 Hook</h5>

[官網](https://zh-hant.reactjs.org/docs/hooks-rules.html)

<h3>useReduer</h3>

```bash
import React,{useReducer} from 'react';

const App = () =>{
   const initialState = { count: 0 };

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

<h3>打造自己的Hook</h3>

[官網](https://zh-hant.reactjs.org/docs/hooks-custom.html)

<h3>常見的hook</h3>

```bash
useState:取代當前的state
useEffect:每次render時，執行一次
useContext:
少見hook
useReducer:
useCallback:
useMemo:
useRef:
useImperativeHandle:
useLayoutEffect:
useDebugValue:
```
 
[官方網站](https://zh-hant.reactjs.org/docs/hooks-intro.html)
