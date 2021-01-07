<h1>組件化</h1>

<h4>以TodoList為例</h4>

App.js
```bash
import React,{Component} from 'react';
import TodoItem from './TodoItem';

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
                // <li key={index} onClick={this.handleItemDelete.bind(this,index)}>{item}</li>
                //組件化
                <div>
                  <TodoItem 
                  content={item} 
                  index={index}
                  deleteItem={this.handleItemDelete.bind(this)}
                  />
                </div>
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
      list:[...this.state.list , this.state.inputValue],
      //list:[先前的數組,input內的值]
      inputValue:''
    })
  }
  點擊li刪除事件
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

TodoItem.js
```bash
import React ,{Component} from 'react';

class TodoItem extends Component{
    constructor(props){
        super(props);
        this.handleClick = this.handleClick.bind(this);
    }
    render(){
        return(
        <div onClick={this.handleClick}>
            {this.props.content}
        </div>
        )
        
    }
    handleClick(){
        this.props.deleteItem(this.props.index);
    }
}
export default TodoItem;
```
