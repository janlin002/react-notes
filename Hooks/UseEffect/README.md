<h3>useEffect</h3>
通常使用於發送api請求<br>
將在每次 render() 後，執行! 

```bash
useEffect 內的 function 會在組件渲染完(render)後被呼叫
```
```bash
useEffect(<didUpdate>, [dependencies])
dependencies = 它是一個陣列，只要每次重新渲染後 dependencies 內的元素沒有改變，任何 useEffect 裡面的函式就不會被執行!
=> 組件渲染完後，如果 dependencies 有改變，才會呼叫 useEffect 內的 function
```

```bash
  useEffect(()=>{
      //組件掛載
    return()=>{
      //組件卸載
    }
  })
```

<h3>用useEffect取代生命週期</h3>

```bash
useEffect() = componentDidMount + componentDidUpdate + componentWillUnmount
```

<h4>無需清除的 Effect</h4>

```bash
=> componentDidMount + componentDidUpdate
```

用意：有時候，我們希望在 React 更新 DOM 之後執行一些額外的程式碼。

<h4>需清除的 Effect</h4>

```bash
=> componentDidMount + componentDidUpdate + componentWillUnmount
```

用意：我們可能想要設定對某些外部資料來源的 [subscription]。在這種情況下，請務必進行清除，以免造成 memory leak！

[官網](https://zh-hant.reactjs.org/docs/hooks-effect.html)

[it鐵人幫](https://ithelp.ithome.com.tw/articles/10245832)
