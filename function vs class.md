<h1>function component 轉換成 class component</h1>

```bash
1.加入 render()
2.function 內容班到 render() 中
3.將 props 改成 this.props
4.刪除 function 宣告
```

<h1> 主要差別 </h1>

```bash
class 需要 render(),function不用
class有this,function沒有
```

[參考文章](https://ithelp.ithome.com.tw/articles/10234746)
[官方參考文章](https://zh-hant.reactjs.org/docs/state-and-lifecycle.html)