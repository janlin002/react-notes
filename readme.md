<h2>Create React App</h2>

```bash
npx create-react-app todolist(資料夾名稱)
cd todolist
npm start
```
(目前版本有點問題，還在找解法中...)
->目前webpack版本不合適，降為4.44.2版就可以了

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

<h1>Proptypes vs defaultProps</h1>

```bash
Proptypes:使用PropTypes進行型別檢查
defaultProps:可為組件增加默認props,一般用於props未賦值,但不能為null的情況
```

<h1>props,state,render關係</h1>

當 props,state 更改時，render一定會重新執行<br>
當父組件的render被運行時，子組件的render一樣會被運行

