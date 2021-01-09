<h1>Redux</h1>

![lifecircle](https://mdimg.wxwenku.com/getimg/ccdf080c7af7e8a10e9b88444af98393461258747dab79fb801805e11763c28eda23f64fa3fd1ebbf7a1f071f9833c42.jpg)

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

<h4>React Component</h4>
畫面
<h4>Action Creater</h4>
告知的行為
<h4>Store</h4>

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
import Store from './store';
constructor(props){
    super(props);
    this.state = store.getStore(); //store數據綁定
}
```

<h4>Reducers</h4>

```bash
創建 store/reducer.js
const defaultState = {}

export default (state = defaultState,action)=>{
    return state
}
```





