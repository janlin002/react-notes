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

<h4>React Component</h4>
畫面
<h4>Action Creater</h4>
告知的行為
<h4>Store</h4>
只會有一個store
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

<h4>Reducers</h4>

只能接受state,但不能改變state

```bash
創建 store/reducer.js
const defaultState = {
    //如同state(資料庫)
}

export default (state = defaultState,action)=>{
    return state
}
```
＝＝＝＝＝＝
<h4>完整程式碼</h4>

```bash
import React ,{Component} from 'react';
import { Input } from 'antd';
import { Button } from 'antd';
import { List, Divider } from 'antd';
import store from './store';

class App extends Component{
  constructor(props){
    super(props);
    this.state = store.getState();
    store.subscribe(this.storeChange); //訂閱
  }
  render(){
    return (
      <div>
          <Input placeholder={this.state.inputValue} style={{width:'300px'}} />
          <Button type="primary">submit</Button>
          <List
            size="small"
            style={{width:'300px'}}
            bordered
            dataSource={this.state.list}
            renderItem={item => <List.Item>{item}</List.Item>}
          />
      </div>
      
    )
  }
}

export default App;
```

index.js

```bash
import { createStore } from 'redux';
import reducer from './reducer';
const store = createStore(reducer);

export default store;
```

reducer.js

```bash
const defaultState = {
    inputValue:'',
    list:[]
}

export default (state = defaultState,action)=>{
    return state;
}
```

[compose](https://chentsulin.github.io/redux/docs/api/compose.html)





