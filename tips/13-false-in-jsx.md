# False in JSX

Here's how `false` renders in different situations:

Renders as `id="false"`:

```javascript
ReactDOM.render(<div id={false} />, mountNode);
```

String `"false"` as input value:

```javascript
ReactDOM.render(<input value={false} />, mountNode);
```

No child:

```javascript
ReactDOM.render(<div>{false}</div>, mountNode);
```

The reason why this one doesn't render as the string `"false"` as a `div` child is to allow the more common use-case: `<div>{x > 1 && 'You have more than one item'}</div>`.
