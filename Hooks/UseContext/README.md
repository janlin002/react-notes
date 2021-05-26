<h3>useContext</h3>

[參考文章](https://medium.com/hannah-lin/react-hook-%E7%AD%86%E8%A8%98-usecontext-4bc289976847)

是用來接收與父 Component 傳遞資料時的 Hooks ，用途和 Props 相同<br>

```bash
// 父層

import React, { useState , createContext } from 'react';

const CountContext = React.createContext()

function Example(){
    const [ count , setCount ] = useState(0);

    return (
        <div>
            <p>You clicked {count} times</p>
            <button onClick={()=>{setCount(count+1)}}>click me</button>

            <CountContext.Provider value={count}> // 把count當作value往下傳
              <Counter /> // 接收value的Component
            </CountContext.Provider>

        </div>
    )
}
export default Example;

//子層: useContext(Abc)接收
import React, { useContext } from 'react';

function Counter() {
    const count = useContext(CountContext); //接收父層的value
    return (<h2>{count}</h2>)
}
```

[參考文件](https://medium.com/enjoy-life-enjoy-coding/react-%E5%9C%A8-hooks-%E4%B8%AD%E4%BB%A5-usecontext-%E8%88%87-usereducer-%E5%AF%A6%E7%8F%BE-redux-3a8aa403d9e4)

[部落格](https://iamian.cc/reactcontextapi/)
