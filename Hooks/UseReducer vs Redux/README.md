# Redux vs useReducer

[推薦文章](https://medium.com/hannah-lin/react-hook-%E7%AD%86%E8%A8%98-usereducer-%E7%9C%9F%E7%9A%84%E8%83%BD%E5%AE%8C%E5%85%A8%E5%8F%96%E4%BB%A3-redux-%E5%97%8E-fabcc1e9b400)

## Redux

> 全域，且可執行 middleware

## useReducer

> 進階版 useState

> 非全域，需搭配 useContext，但因為 useContext 有有渲染問題(父元素渲染影響子元素)，所以目前沒機會取代 useReducer
