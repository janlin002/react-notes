<h1>Jest邏輯</h1>

[jaspar文章](https://wcc723.github.io/development/2020/02/02/jest-intro/)

[官方網站](https://jestjs.io/)

[Matchers](https://jestjs.io/docs/using-matchers)

```bash
測試的目標為何？ -> test('...', ()=>{})
導入要測試的函式 -> employee.makeChange()
測試的期望是什麼？ -> expect(...).toBe(...);
```

範例

```bash
const employee = {
  makeChange: function(bill, price) {
    return bill - price;
  }
};

export default employee;


import employee from './xxx/;

// 明確描述測試的目標：'拿 200 元買套餐，預期會找 73 元'
test('拿 200 元買套餐，預期會找 73 元', () => {
  const bill = 200;  // 小明手中的鈔票
  const price = 127; // 餐點的價格

  // 期望找錢的結果是符合預期的
  expect(employee.makeChange(bill, price)).toBe(73);
});
```

