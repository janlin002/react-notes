<h2>使用jest</h2>

<h3>導入jest</h3>

```bash
npm install jest --save-dev
```

在package.json中加入jest(單一監控)

```bash
{
  "devDependencies": {
    "jest": "^24.9.0"
  },
  "scripts": {
    "test": "jest" // 運行 test 的方法時，會使用 jest 作為套件開始運行
  },
  // ...
}
```

執行
```bash
npm run test
```

持續監控

```bash
{
  "devDependencies": {
    "jest": "^24.9.0"
  },
  "scripts": {
    "testwatch": "jest --watchAll"
 // 使用 npm run testwatch 時會持續用監控的形式，而不是只有單一次報告
  },
  // ...
}
```