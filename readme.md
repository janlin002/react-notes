<h2>Create React App</h2>

```bash
npx create-react-app todolist(資料夾名稱)
cd todolist
npm start
```
(目前版本有點問題，還在找解法中...)

<<<<<<< HEAD
<h1>React 環境建置</h1>

```bash
<html>
  <head>
    <meta charset="utf-8" />

    <title>React_CDN</title>

    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6.26.0/babel.js"></script>
  </head>

  <body>
    <div id="root"></div>

    <script type="text/babel">
      // React code will go here
    </script>

  </body>
</html>
```

[參考文章](https://askie.today/react-setting-cdn-and-creatreactapp/)


=======
function component 轉換成 class component

```bash
1.加入 render()
2.function 內容班到 render() 中
3.將 props 改成 this.props
4.刪除 function 宣告
```
>>>>>>> cd5014f961afe9eacdb06d067c570302a60d4dd0
