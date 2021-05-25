<h1>非同步</h1>

<h3>sync vs async</h3>

sync: 同步<br>
async: 非同步

<h3>async</h3>

<h3>await</h3>
await是在等待一個async函數的完成<br>
await 一定得運行在 async function 內！

```bash
//順序
async function a(){
  await b();
  .....       // 等 b() 完成後才會執行
  await c();
  .....       // 等 c() 完成後才會執行
  await new Promise(resolve=>{
    .....
  });
  .....       // 上方的 promise 完成後才會執行
}
a();
a().then(()=>{
  .....       // 等 a() 完成後接著執行
});
```

```bash
// 實際例子
function takeLongTime() {
    return new Promise(resolve => {
        setTimeout(() => resolve("long_time_value"), 1000);
    });
}

async function test() {
    const v = await takeLongTime();
    console.log(v);
}

test();
```