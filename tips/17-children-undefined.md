# this.props.children undefined

You can't access the children of your component through `this.props.children`. `this.props.children` designates the children being **passed onto you** by the owner:

```js
var App = React.createClass({
  componentDidMount: function() {
    // This doesn't refer to the `span`s! It refers to the children between
    // last line's `<App></App>`, which are undefined.
    console.log(this.props.children);
  },

  render: function() {
    return <div><span/><span/></div>;
  }
});

ReactDOM.render(<App></App>, mountNode);
```

To access your own subcomponents (the `span`s), place [refs](../docs/08.1-more-about-refs.md) on them.
