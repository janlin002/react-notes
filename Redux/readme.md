<h1>Redux</h1>

Reducers + Flux

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

<h4>React Component</h4>

<h4>Action Creater</h4>

<h4>Store</h4>

```bash
創建store
建立 store/index.js
import {createStore} from 'redux';
import reducer from './reducer';

const store = createStore(reducer);
export store
```

<h4>Reducers</h4>

```bash
創建 store/reducer.js
const defaultState = {}

export default (state = defaultState,action)=>{
    return state
}
```



![lifecircle](https://img-blog.csdn.net/20181005205138574?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0hlbGxveW9uZ3dlaQ==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

