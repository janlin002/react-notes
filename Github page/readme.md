<h3>router相關問題</h3>

[推薦文章](https://medium.com/@arijit_chowdhury/deploy-react-app-with-react-router-to-github-pages-for-free-569377f483f)

<h3>下載gh-pages</h3>

```bash
npm install --save-dev gh-pages
```

<h3>在package.json內加入homepage</h3>

```bash
"homepage": "http://your-username.github.io/myapp",
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
