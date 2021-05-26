<h3>useCallback</h3>

useCallback 其實就等於回傳一個 function 的 useMemo<br>
主要目的是避免在 component 內部宣告的 function

```bash
useCallback(fn, deps) 等同於 useMemo(() => fn, deps)
```