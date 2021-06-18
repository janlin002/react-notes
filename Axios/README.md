<h2>Use Axios in react</h2>

```bash
npm install axios

yarn add axios
```

<h3>simple GET request using Axios</h3>

use in Life-Cycle - componentDidMount

```bash
componentDidMount() {
    // Simple GET request using axios
    axios.get('https://api.npms.io/v2/search?q=react')
        .then(response => this.setState({ totalReactPackages: response.data.total }));
}
```

<h3>use Axios in React-hooks</h3>

```bash
useEffect(() => {
    // GET request using axios inside useEffect React hook
    axios.get('https://api.npms.io/v2/search?q=react')
        .then(response => setTotalReactPackages(response.data.total));
}, []);
```

<h3>use Axios-hooks</h3>

[Link](https://www.npmjs.com/package/axios-hooks)

```bash
npm install axios axios-hooks
```


