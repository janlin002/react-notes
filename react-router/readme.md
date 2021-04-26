<h2>React路由</h2>

[官網](https://reactrouter.com/web/api/Redirect)

[react-router(上)](https://ithelp.ithome.com.tw/articles/10226056)

[react-router(下)](https://ithelp.ithome.com.tw/articles/10226370)

[Router初探](https://ithelp.ithome.com.tw/articles/10247735)

[react-router-dom](https://medium.com/%E6%89%8B%E5%AF%AB%E7%AD%86%E8%A8%98/a-little-bit-of-react-router-dom-e5b809fcb127)

<h2>文檔</h2>

[中文文檔](https://react-guide.github.io/react-router-cn/) -- 不推薦，文檔沒更新

[入門實戰-Github](https://github.com/kdchang/reactjs101/blob/master/Ch05/react-router-introduction.md)

[Github中文版翻譯](https://github.com/react-translate-team/react-router-CN)

<h2>影音版</h2>

[技術胖](https://www.bilibili.com/video/BV1Z4411f7T5?from=search&seid=16845280384785881034)

[技術胖文檔](https://jspang.com/detailed?id=49) -- 可搭配上面的影片



<h2>安裝</h2>

```bash
npm install --save react-router-dom
```

```bash
// 使用 ES6 的轉譯器，如 babel
import { Router, Route, Link } from 'react-router'

// 不使用 ES6 的轉譯器
var ReactRouter = require('react-router')
var Router = ReactRouter.Router
var Route = ReactRouter.Route
var Link = ReactRouter.Link
```

<h2>react-router vs react-router-dom</h2>

[文章](https://www.ucamc.com/e-learning/javascript/278-%E7%B0%A1%E5%96%AE%E4%BB%8B%E7%B4%B9%E4%BA%86%E8%A7%A3react-router-4%E6%95%99%E5%AD%B8)

[Github issue](https://github.com/mrdulin/blog/issues/42)

react-router-dom比react-router多了 BrowserRouter、 HashRouter、Link、NavLink;<br>

