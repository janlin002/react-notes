```bash
import React, {useState, useCallback} from 'react';

function App (){
    const [count, setCount] = useState(0);
    const callbackTest = useCallback(()=>{
        console.log(count);
        return count;
    }, [count])

    return (
        <div>
            <h1>{count}</h1>
            <h1>{callbackTest()}</h1>
            <button onClick={()=>{setCount(count + 1)}}>+1</button>
        </div>
    )

}
export default App;
```

和useMemo差別：

```bash
useMemo: const xxx = useMemo(()=>ooo(abc), [abc]);

// 為一個function
useCallback: const xxx = useCallback(()=>{
    return ooo;
}, [abc]) 
```