<h1>redux 與 axios結合</h1>

[官方網站](https://github.com/axios/axios)

<h2>Download</h2>

```bash
npm install axios --save
```

<h2>引入axios</h2>

```bash
import axios from 'axios'
```

```bash
componentDidMount() {
    axios.get('xxx').then((res)=>{
        xxx
    })
}
```

<h2>axios與redux結合</h2>

首先先建立一個action<br>

```bash
export const getListAction  = (data)=>({
    type:GET_LIST,
    data
})
```

並且寫入actionTypes.js<br>

```bash
const GET_LIST = 'GET_LIST'
```

並且寫入actionTypes.js<br>

```bash
import { getListAction } from './actionCreator';
```

把action加入到axios中

```bash
componentDidMount(){
    axios.get('xxx').then((res)=>{    
        const data = res.data
        const action = getListAction(data)
        store.dispatch(action)
    })
}
```
