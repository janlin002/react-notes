<h1>Redux</h1>

![清晰版](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/4b8a429c6db8412e9b31e6983da75b0a~tplv-k3u1fbpfcp-zoom-1.image)

<h4>Redux環境建立</h4>

```bash
npm install --save redux
```

<h4>Redux vs React-Redux</h4>

React-Redux是為了串連 React 跟 Redux;
[參考文章]()

<h4>Redux環境建立</h4>

```bash
npm install --save react-redux
npm install --save-dev redux-devtools
```
[好文分享](https://www.mdeditor.tw/pl/2Fqz/zh-tw)

[redux vs react-redux](https://segmentfault.com/a/1190000011473973)

<h2>整體流程(未包含 react-redux)</h2>

```bash
store.dispatch(); 將action傳到reducer
store.getState(); store綁定component, 取得reducer中的資料
=> this.state = store.getState(); // 綁定state
```

<h4>React Component</h4>
畫面
<h1>Action</h1>
告知的行為

```bash
const action = {
    type: 'SEND_ACTION',
}
store.dispatch(action) // 把action傳給store
```

<h1>Store</h1>

只會有一個store<br>
一定是純函數（給訂一定的輸入，一定會有輸出，且不會有副作用）

```bash
創建store
建立 store/index.js
import {createStore} from 'redux';
import reducer from './reducer';

const store = createStore(reducer);
export default store
```

```bash
取得store的數據
App.js
import store from './store';
constructor(props){
    super(props);
    this.state = store.getStore(); //store數據綁定
}
```

<h1>Reducers</h1>

只能接受state,但不能改變state

```bash
創建 store/reducer.js
const defaultState = {
    //如同state(資料庫)
}

export default (state = defaultState,action)=>{
    switch (action.type) {
        case value:
            
            break;
    
        default:
            break;
    }
}
```
<h1>Action集中管理</h1>
<h1>方法一</h1>

需先建立一個資料夾 - actionTypes.js<br>
將action 的 type 加入其中

```bash
export const ADD_TODOITEM = 'ADD_TODOITEM'
export const REMOVE_TODOITEM = 'REMOVE_TODOITEM'
```
在需要用到的 Component 中引入

```bash
import { ADD_TODOITEM, REMOVE_TODOITEM } from './actionTypes'
```
需更改原先action的type(reducer也可更改)

<h1>方法二</h1>

需先建立一個資料夾 - actionCreator<br>
導入方法一的 actionTypes.js資料夾,並且寫下action的function

```bash
import { ADD_TODOITEM, REMOVE_TODOITEM } from './actionTypes'

export const addToDoItem = () =>{
    return {
        type: ADD_TODOITEM
    }
}
```

回到需導入 action 的 Component 導入 新的function

```bash
import { addToDoItem } from './actionCreator'
```

並到需要觸發action的function內進行導入

```bash
addAction = () =>{
    const addTodoItem = addTodoItem();
    store.dispatch(addTodoItem); // store.dispatch(addTodoItem())
}
```









[compose](https://chentsulin.github.io/redux/docs/api/compose.html)





