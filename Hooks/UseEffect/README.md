<h3>useEffect</h3>
語法
```bash
  useEffect(()=>{
      //組件掛載
    return()=>{
      //組件卸載
    }
  }, [])
```

<h3>用useEffect取代生命週期</h3>

```bash
useEffect() = componentDidMount + componentDidUpdate + (componentWillUnmount)
```

<h4>無需清除的 Effect</h4>

```bash
=> componentDidMount + componentDidUpdate
```

```bash
useEffect(()=>{
    console.log('無需清除')
})
```

用意：有時候，我們希望在 React 更新 DOM 之後執行一些額外的程式碼。

<h4>需清除的 Effect</h4>

```bash
=> componentDidMount + componentDidUpdate + componentWillUnmount
```

```bash
useEffect(()=>{
    console.log('需清除');
    return ()=>{
        console.log('卸載時顯示（離開時顯示）')
    }
})
```

用意：我們可能想要設定對某些外部資料來源的 [subscription]。在這種情況下，請務必進行清除，以免造成 memory leak！

<h4>第二個參數 []</h4>

用意：實現 componentWillUnmount<br>

當 [] 內有東西：只有在 [] 內的東西改變時，才重新訂閱;
當 [] 為空：當畫面有改變才會重新訂閱;

```bash
useEffect(()=>{
    console.log('需清除');
    return ()=>{
        console.log('卸載時顯示（離開時顯示）')
    }
}, [])

```bash
useEffect(<didUpdate>, [dependencies])
dependencies = 它是一個陣列，只要每次重新渲染後 dependencies 內的元素沒有改變，任何 useEffect 裡面的函式就不會被執行!
=> 組件渲染完後，如果 dependencies 有改變，才會呼叫 useEffect 內的 function
```




[官網](https://zh-hant.reactjs.org/docs/hooks-effect.html)

[it鐵人幫](https://ithelp.ithome.com.tw/articles/10245832)
