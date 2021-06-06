<h3>useDispatch</h3>

[文章](https://ithelp.ithome.com.tw/articles/10251966)

```bash
const dispatch = useDispatch();

 <button onClick={() => dispatch({ type: 'xxx' }  )}>
        xxxx
 </button>
```
可以用來取代掉 mapStateToDispatch<br>
＝>因為砍掉 mapDispatchToProps ,所以改用 useDispatch 來觸發Reducer
