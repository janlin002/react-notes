<h2>實例</h2>

[Demo]()

```bash
import React, {useRef, useState, useEffect} from 'react';

function App (){
    const refValue = useRef(null);
    const [text, setText] = useState('jspang')
    const textRef = useRef()

    useEffect(()=>{
        textRef.current = text;
        console.log('textRef.current:', textRef.current)
    })
    const buttonClick=()=>{
        refValue.current.value = 'hello';
        console.log(refValue,'refValue');
    }
    const inputChange =(e)=>{
        console.log(e.target.value)
    }
    return (
        <div>
            <input type="text" ref={refValue} onChange={inputChange}/>
            <button onClick={buttonClick}>顯示文字</button>
            <input value={text} onChange={(e)=>{setText(e.target.value)}} />
        </div>
    )
}

export default App;
```