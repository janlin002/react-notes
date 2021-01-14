<h1>actionTypes</h1>

<h4>用意</h4>
方便測試，管理action

<h4>步驟</h4>

1.建立一個 ./store/actionTypes.js 的資料夾<br>

2.把 action 事件載入<br>

```bash
export const CHANGE_INPUT_VALUE = 'change_input_value';
export const ADD_TODO_ITEM = 'add_todo_item';
export const DELETE_TODO_ITEM = 'delete_todo_item';
```

3.在 App.js 中載入 actionTypes.js 的資料<br>

```bash
import {CHANGE_INPUT_VALUE , ADD_TODO_ITEM , DELETE_TODO_ITEM} from './store/actionTypes'
```

4.把 action 中的 type 換成載入的元素<br>

```bash
const action = {
      type:'change_input_value', ==> type:CHANGE_INPUT_VALUE,
      value:e.target.value
    }
```

5.reducer 的 action 也須一併修改<br>

6.完成<br>


[參考文章](https://ithelp.ithome.com.tw/articles/10250728)
