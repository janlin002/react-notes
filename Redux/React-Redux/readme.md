<h2>React-redux</h2>

目的:程式優化<br>

<h3>環境:</h3>

npm install --save react-redux

<h3>Provider -- 提供者</h3>
可以使你整個APP都接收到Store中的數據<br>
接收store作為props

<h3>Connect -- 接收者</h3>
組件跟Store進行綁定<br>
方便組件取得store中的state<br>

```bash
connect(要接受數組的函式,要發送action的函式)(放入要加強的組件)
```

```bash
connect參數:
mapStateToProps - 傳state
mapDispatchToProps - 傳actions
mergeProps
options
```



