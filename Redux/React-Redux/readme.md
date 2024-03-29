<h2>React-redux</h2>

目的:程式優化<br>

(可刪除 this.state = store.getState())

<h3>DownLoad</h3>

[NPM](https://www.npmjs.com/package/react-redux)

```javascript
npm install react-redux --save
```

<h3>Provider -- 提供者</h3>
可以使你整個APP都接收到Store中的數據<br>
接收store作為props<br>
需包覆在最外層

```javascript
//再最外層的index.js加入Provider

import React from "react";
import ReactDOM from "react-dom";

import { Provider } from "react-redux"; // 1.
import store from "./src/store";  // 2.

import App from "./App";

ReactDOM.render(
  <Provider store={store}>  { /* 將store作為props傳遞給其他component */ }
    <App />
  </Provider>,
  document.getElementById("app")
);
```

### Connect -- 接收者
組件跟Store進行綁定<br>
方便組件取得store中的state<br>

```javascript
import { connect } from 'react-redux'
connect(要接受數組的函式)(要發送action的函式)(放入要加強的組件)
ex.connect(mapStateToProps)(Component)
```
## connect參數:

<h4>1.mapStateToProps</h4>
這個函式允許我們將 store 中的數據作為 props 綁到指定的組件上

```javascript
const initState = {
    name: 'Jack',
}

const mapStateToProps = state => ({
    name: state.name
})

{this.props.name} // 可用props調用 reducer中的函數
```
連接component和mapStateToProps = connect

```javascript
import { connect } from 'react-redux'

const Title = connect(mapStateToProps)(Component)

export default Title;
```


<h4>2.mapDispatchToProps</h4>
將 action 作為 props 綁到自己的函式中
<h4>3.mergeProps</h4>

<h4>4.options</h4>



