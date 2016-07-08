# Value of null for Controlled Input

Specifying the `value` prop on a [controlled component](../docs/07-forms.md) prevents the user from changing the input unless you desire so.

You might have run into a problem where `value` is specified, but the input can still be changed without consent. In this case, you might have accidentally set `value` to `undefined` or `null`.

The snippet below shows this phenomenon; after a second, the text becomes editable.

```javascript
ReactDOM.render(<input value="hi" />, mountNode);

setTimeout(function() {
  ReactDOM.render(<input value={null} />, mountNode);
}, 1000);
```
