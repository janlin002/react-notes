<h1>Hook</h1>
<h3>Hook 是 React 16.8 中增加的新功能。它讓你不必寫 class 就能使用 state 以及其他 React 的功能。</h3>

<h3>影音資源</h3>

[技術胖](https://www.bilibili.com/video/BV1y4411Q7yH?from=search&seid=15129246938121288056)

[合一大師](https://www.bilibili.com/video/BV1ca4y1Y7R1?p=3)

[老菜鳥](https://www.bilibili.com/video/BV1VE411w7wi?from=search&seid=15129246938121288056)

<h3>那...為什麼要Hook?</h3>

[技術文章](https://www.mdeditor.tw/pl/pG7r/zh-tw)

[Medium](https://snh90100.medium.com/%E5%B8%B8%E8%A6%8B%E7%9A%84%E5%B9%BE%E5%80%8B-react-hooks-%E4%BB%8B%E7%B4%B9-usestate-useeffect-useref-40c9acd0cc4c)

<h3>Hook簡介</h3>
Hook 是 JavaScript function<br>

1.只在 最上層 呼叫 Hook。不要在迴圈、判斷式、或是嵌套 function 中呼叫 Hook。<br>
2.只在 React function component 呼叫 Hook。不要在一般 JavaScript function 中呼叫 Hook。

<h3>Hook規則</h3>
<h5>只在最上層呼叫 Hook</h5>
<h5>只在 React Function 中呼叫 Hook</h5>

[官網](https://zh-hant.reactjs.org/docs/hooks-rules.html)

<h3>useContext</h3>

```bash
是用來接收與父 Component 傳遞資料時的 Hooks ，用途和 Props 相同<br>
如同<Abc/>
父層: <Abc.provider value傳遞 /> => 子層: useContext(Abc)接收
```

[參考文件](https://medium.com/enjoy-life-enjoy-coding/react-%E5%9C%A8-hooks-%E4%B8%AD%E4%BB%A5-usecontext-%E8%88%87-usereducer-%E5%AF%A6%E7%8F%BE-redux-3a8aa403d9e4)

[部落格](https://iamian.cc/reactcontextapi/)

<h3>useReduer</h3>

useState 的替代方案。它接收一个形如 (state, action) => newState 的 reducer，并返回当前的 state 以及与其配套的 dispatch 方法。

```bash
const [state, dispatch] = useReducer(reducer, initialState);
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
<h3>useMemo</h3>

他的目的是用來「避免重複進行複雜耗時的計算」,保存計算結果<br>
useMemo 會在組件渲染時（rendering）被呼叫，因此不應該在這個時間點進行任何會有副作用（side effect）的操作；若需要有副作用的操作，則應該使用的是 useEffect 而不是 useMemo。

<h3>useCallback</h3>

useCallback 其實就等於回傳一個 function 的 useMemo<br>
主要目的是避免在 component 內部宣告的 function

```bash
useCallback(fn, deps) 等同於 useMemo(() => fn, deps)
```

<h3>useRef</h3>

存放可變的值

[it-ironman](https://ithelp.ithome.com.tw/articles/10219187)

<h3>useSelector</h3>

這個方法允許我們直接從 Redux store 中的狀態提取數據到元件中。透過 useSelector 可以取代掉 mapStateToProps 的使用方式 -->(取代掉 mapStateToProps , mapDispatchToProps )

<h3>useDispatch</h3>

可以用來取代掉 mapStateToDispatch -->(因為砍掉 mapDispatchToProps ,所以改用 useDispatch 來觸發Reducer)

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
