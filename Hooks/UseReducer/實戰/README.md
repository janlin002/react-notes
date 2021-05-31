<h1> 使用useContext 跟 useReducer 實現 切換顏色的效果</h1>

[Demo](https://codesandbox.io/embed/crazy-cookies-oyg3l?fontsize=14&hidenavigation=1&theme=dark)

<h3>需先建立4個資料夾</h3>
<ol>
    <li>文字檔案-(Text.js)</li>
    <li>按鈕檔案-(Button.js)</li>
    <li>顏色邏輯檔案-(changeColor.js)</li>
    <li>統合檔案-(All.js)</li>
</ol>

<h3>目的</h3>
點擊按鈕時，切換顏色

<h3>初始程式碼</h3>

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

<h3>加入useContext, useReducer</h3>

changeColor.js

```bash
import React from 'react';

export const changeColor = React.createContext({});

export const UPDATE_COLOR = 'UPDATE_COLOR';

export const reducer = (state, action) =>{
    switch(action.type){
        case UPDATE_COLOR:
            return action.color;
        default:
            return state;
    }
}

export const Color = props =>{ (把value傳到props.children中)
    const [ color, dispatch ] = useReducer(reducer, 'blue');
    return (
        <changeColor.Provider value={{color, dispatch}}>
            {props.children}
        </changeColor.Provider>
    )
}

```

All.js

```bash
import React from 'react';
import Text from './Text';
import Button from './Button';
import { Color } from './changeColor';

function All (){
    return (
        <div>
            <Color> (Color內的component都會接收到Color傳過來的資料)
                <Text />
                <Button />
            </Color>
        </div>
    )
}

export default All;

```

Text.js

```bash
import React, {useContext} from 'react';
import { changeColor } from './changeColor';

function Text(){
    const { color } = useContext(changeColor);
    return (
        <div style={{color: color}}>
            這是{color}色
        </div>
    )
}

export default Text;
```

Button.js

```bash
import React, { useContext } from 'react';
import { changeColor, UPDATE_COLOR } from './changeColor';


function Button (){
    const { dispatch } = useContext(changeColor)
    return (
        <div>
            <button onClick={()=>{dispatch({type: UPDATE_COLOR, color: 'red'})}}>紅色</button>
            <button onClick={()=>{dispatch({type: UPDATE_COLOR, color: 'green'})}}>綠色</button>
        </div>
    )
}

export default Button;
```
