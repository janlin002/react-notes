<h2>Create React App</h2>

```bash
npx create-react-app todolist(資料夾名稱)
cd todolist
npm start
```
(目前版本有點問題，還在找解法中...)

<h1>React 環境建置</h1>

```bash
<html>
  <head>
    <meta charset="utf-8" />

    <title>React_CDN</title>

    <script src="https://unpkg.com/react@16/umd/react.development.js"></script>
    <script src="https://unpkg.com/react-dom@16/umd/react-dom.development.js"></script>
    <script src="https://unpkg.com/babel-standalone@6.26.0/babel.js"></script>
  </head>

  <body>
    <div id="root"></div>

    <script type="text/babel">
      // React code will go here
    </script>

  </body>
</html>
```

[參考文章](https://askie.today/react-setting-cdn-and-creatreactapp/)


function component 轉換成 class component

```bash
1.加入 render()
2.function 內容班到 render() 中
3.將 props 改成 this.props
4.刪除 function 宣告
```
<h1>TodoList</h1>

```bash
import React,{Component} from 'react';

class App extends Component{

  constructor(props){
    super(props);
    this.state={
      inputValue:'',
      list:[]
    }
  }
  render(){
    return(
      <div>
        <input 
        //input的值
        value={this.state.inputValue}
        //當輸入後的變化
        onChange={this.handleInputChange.bind(this)}
        />
        <button onClick={this.handleBtnClick.bind(this)}>
          提交
        </button>
        <ul>
          {
            this.state.list.map((item,index)=>{
              return(
                <li key={index} onClick={this.handleItemDelete.bind(this,index)}>{item}</li>
              ) 
            })
          }
        </ul>
      </div>
    )
  }
  //畫面綁定
  handleInputChange(e){
    this.setState({
      inputValue : e.target.value
    })
  }
  //點擊新增事件
  handleBtnClick(){
    this.setState({
      list:[...this.state.list,this.state.inputValue],
      //list:[先前的數組,input內的值]
      inputValue:''
    })
  }
  //點擊li刪除事件
  handleItemDelete(index){
    // console.log(index);
    const list = [...this.state.list];
    list.splice(index,1);
    this.setState({
      list:list
    })

  }
}

export default App;
```
