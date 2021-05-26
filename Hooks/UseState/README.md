<h3>useState</h3>

function 中的 [useState] 如同 class 中的 [this.state];<br>

```bash
import React, {useState} from 'react';

const [count, SetCount] = useState(0);

=> const [回傳的值,可以更新state的function] = useState(預設值)
```

[官網](https://zh-hant.reactjs.org/docs/hooks-state.html)
