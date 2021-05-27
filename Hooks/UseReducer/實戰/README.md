<h1> 使用useContext 跟 useReducer 實現 切換顏色的效果</h1>

<h4>需先建立4個資料夾</h4>
<ol>
    <li>文字檔案-(Text.js)</li>
    <li>按鈕檔案-(Button.js)</li>
    <li>顏色邏輯檔案-(changeColor.js)</li>
    <li>統合檔案-(All.js)</li>
</ol>

<h4>目的</h4>
點擊按鈕時，切換顏色

<h4>初始程式碼</h4>

Text.js

```bash
import React from 'react';

function Text(){
    return (
        <div style={{color:'black'}}>
            這是藍色
        </div>
    )
}

export default Text;
```

Button.js

```bash
import React from 'react';

function Button (){
    return (
        <div>
            <button>紅色</button>
            <button>綠色</button>
        </div>
    )
}

export default Button;
```

All.js

```bash
import React from 'react';
import Text from './Text';
import Button from './Button';

function All (){
    return (
        <div>
            <Text />
            <Button />
        </div>
    )
}

export default All;
```

<h4>加入useContext, useReducer</h4>
