<h2>動態傳值</h2>

```bash
这个设置是以:开始的，然后紧跟着你传递的key（键名称）名称。
===>
<Route path="/list/:id" component={List} />
<li><Link to="/list/123">列表</Link> </li>
```

```bash
List.js:
componentDidMount(){
        let tempId = this.props.match.params.id;
        this.setState({id:tempId });
    }
```

