<h2>exact 精准匹配</h2>

顧名思義：路由訊息要完全匹配才會跳轉，指匹配一部分是不行的<br>

```bash
正常版：http://localhost:3000/#/
有加exact:http://localhost:3000/#/123 =>報錯
沒加exact:http://localhost:3000/#/123 =>不會報錯(會顯示/#/的內容)
```

