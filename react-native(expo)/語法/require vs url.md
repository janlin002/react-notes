## require()
當你要呼叫的圖片是儲存在本地電腦裡的時候，要用的就是require()

```js
<ImageBackground source=require('檔案路徑')> </ImageBackground>
```

## url()
當你要的圖片是位在網路上的時候，要用的就是uri

```js
<ImageBackground source={{ uri: '檔案所在地的網址' }}> </ImageBackground>
```