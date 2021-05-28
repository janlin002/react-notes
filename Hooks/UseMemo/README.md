<h3>useMemo</h3>

[參考文章](https://juejin.cn/post/6844903925871722510)

他的目的是用來「避免重複進行複雜耗時的計算<br>

```bash
避免父組件每次更改數據時都重新render子組件，減少不必要的效能消耗
```

useMemo 會在組件渲染時（rendering）被呼叫，因此不應該在這個時間點進行任何會有副作用（side effect）的操作；若需要有副作用的操作，則應該使用的是 useEffect 而不是 useMemo。

```bash
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);

當[array]內的值改變時，才會重新渲染,如果為空array，每次更改數據都會重新render
```