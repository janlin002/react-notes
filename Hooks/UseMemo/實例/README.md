<h2>UseMemo實例</h2>

[Demo](https://codesandbox.io/s/usememo-om4rz)

```bash
import React, { useState, useMemo } from "react";

function ChildComponent({ name, children }) {
  function acompClick(name) {
    console.log("a被點擊");
    return name + "Ａ被點擊";
  }
  const acompClickHandler = useMemo(() => acompClick(name), [name]);
  return (
    <div>
      <div>{acompClickHandler}</div>
      <div>{children}</div>
    </div>
  );
}

function App() {
  const [acomp, setAcomp] = useState("A組件");
  const [bcomp, setBcomp] = useState("B組件");
  return (
    <div>
      <button
        onClick={() => {
          setAcomp(new Date().getTime());
        }}
      >
        A組件
      </button>
      <button
        onClick={() => {
          setBcomp(new Date().getTime() + ",B組件");
        }}
      >
        B組件
      </button>
      <ChildComponent name={acomp}>{bcomp}</ChildComponent>
    </div>
  );
}

export default App;
// 因為使用了useMemo，所以只有在點擊Ａ組件才會顯示console內的內容
```
