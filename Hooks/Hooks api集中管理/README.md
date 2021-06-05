<h2>需要會技術： UseContext</h2>

原始代碼：<br>
目標希望不要每個頁面前面都寫一堆hooks

App.jsx(方react-router的地方)

```bash
import React from 'react'
import 內容 from './xxx'

function App(){
    return (
        <內容 />
    )
}
export default App;
```

內容：
```bash
import React from 'react'

function Content (){
    return (
        <div>
            xxx
        </div>
    )
}
export default Content;
```