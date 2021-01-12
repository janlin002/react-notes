<h2>Redirect - 重新導向，重定向</h2>

<h2>用意</h2>
Redirect: 用於頁面重整等等時，作為重導向到指定路徑使用

<h2>方法</h2>

1.標籤式重定向

```bash

//路由配置

import Home from './Pages/Home'
<Route path="/home/" component={Home} />

//首頁

import { Link , Redirect } from "react-router-dom";

//首頁的render後

 <Redirect to="/home/" />
```

2.編程式重定向

```bash
 this.props.history.push("/home/"); 
```