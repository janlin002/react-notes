<h2>React-redux</h2>

目的:程式優化<br>

<h3>DownLoad</h3>

```bash
npm install react-redux --save
```

<h3>Provider -- 提供者</h3>
可以使你整個APP都接收到Store中的數據<br>
接收store作為props<br>
需包覆在最外層

<h3>Connect -- 接收者</h3>
組件跟Store進行綁定<br>
方便組件取得store中的state<br>

```bash
connect(要接受數組的函式,要發送action的函式)(放入要加強的組件)
```
<h3>connect參數:</h3>

<h4>1.mapStateToProps</h4>
這個函式允許我們將 store 中的數據作為 props 綁到指定的組件上

```bash
const mapStateToProps = state => ({
    name: state.name
})
```

<h4>2.mapDispatchToProps</h4>
將 action 作為 props 綁到自己的函式中
<h4>3.mergeProps</h4>

<h4>4.options</h4>



