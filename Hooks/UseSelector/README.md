<h3>useSelector</h3>

[文章](https://ithelp.ithome.com.tw/articles/10251966)

```bash
const 取得的變數 ＝ useSelector(state => state.count)
const counter = useSelector(state => state.counter)
取代 mapStateToProps
```

這個方法允許我們直接從 Redux store 中的狀態提取數據到元件中。透過 useSelector 可以取代掉 mapStateToProps 的使用方式
