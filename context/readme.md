<h2>Context</h2>

<h2>文章</h2>

[官網](https://react.html.cn/docs/context.html)

<h2>用意</h2>
在典型的React 應用程序中，數據通過props 自上而下（父到子）傳遞，<br>
但對於應用程序中許多組件所需的某些類型的props（例如環境偏好,UI主題），這可能很麻煩。<br>
上下文(Context) 提供了在組件之間共享這些值的方法，而不必在DOM Tree的每個層級顯示傳遞一個 prop 。

<h2>注意</h2>
當一些數據需要在不同的嵌套級別上被許多組件訪問時，首先考慮使用 Context。<br>
請謹慎使用它，因為它使組件重用更加困難。

<h2>API</h2>

```bash

React.createContext
創建一個 Context 對象。當 React 渲染訂閱這個 Context 對象的組件時，它將從組件樹中匹配最接近的 Provider 中讀取當前的 context 值。

Context.Provider
每個 Context 對像都附帶一個 Provider React組件，允許 consumer(使用者) 組件 來 訂閱 context 的改變。

Class.contextType
可以為類上的 contextType 屬性分配由 React.createContext() 創建的 Context 對象。這允許您使用this.context 使用該 Context 類型 的最近的當前值。您可以在任何生命週期方法中引用它，包括 render 函數。

Context.Consumer
一個可以訂閱 context 變化的 React 組件。
```


