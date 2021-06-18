<h3>router相關問題</h3>

[推薦文章](https://medium.com/@arijit_chowdhury/deploy-react-app-with-react-router-to-github-pages-for-free-569377f483f)

[中文版教學](https://medium.com/@aaa24295234/%E5%B0%87create-react-app%E4%BD%88%E7%BD%B2%E5%88%B0github-pages-1a7ba468861a)

<h3>下載gh-pages</h3>

```bash
npm install --save-dev gh-pages
```

<h3>在package.json內加入homepage</h3>

```bash
"homepage": "http://github名稱.github.io/專案名稱",
```

<h3>在package.json的script中加入：</h3>

```bash
"scripts": {
    ...
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build"
}
```

<h3>每次部署都需加入：</h3>

```bash
npm run deploy
```
