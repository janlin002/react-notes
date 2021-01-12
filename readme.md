<h2>學習資源</h2>

[資源分享](https://github.com/janlin002/react-notes/blob/master/%E8%B3%87%E6%BA%90%E5%88%86%E4%BA%AB.md)

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





