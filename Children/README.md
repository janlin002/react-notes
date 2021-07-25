# Children

[It 鐵人幫](https://ithelp.ithome.com.tw/articles/10218605)

```bash
<元素名稱> (其他的東西) </元素名稱>;

其他的東西 = children;

children是props之一,所以當使用的children改變時，畫面也會重繪。
```

### Index.js

```javascript
import React from 'react';
import ReactDOM from 'react-dom';
import App from './App';

ReactDOM.render(
  <div>
    <App> 在index.js中設定文字 </App>
  </div>,
  document.getElementById('root')
);
```

### App.js

```javascript
import React from 'react';
function App(props) {
  return <button> {props.name} </button>;
}
export default App;
```

### 執行結果

```javascript
在index.js中設定文字;
```
