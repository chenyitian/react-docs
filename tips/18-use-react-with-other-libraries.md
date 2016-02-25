# Use React with Other Libraries

You don't have to go full React. The component [lifecycle events](../docs/ref-03-component-specs.md#lifecycle-methods), especially `componentDidMount` and `componentDidUpdate`, are good places to put your other libraries' logic.

```js
var App = React.createClass({
  getInitialState: function() {
    return {myModel: new myBackboneModel({items: [1, 2, 3]})};
  },

  componentDidMount: function() {
    $(this.refs.placeholder).append($('<span />'));
  },

  componentWillUnmount: function() {
    // Clean up work here.
  },

  shouldComponentUpdate: function() {
    // Let's just never update this component again.
    return false;
  },

  render: function() {
    return <div ref="placeholder"/>;
  }
});

ReactDOM.render(<App />, mountNode);
```

You can attach your own [event listeners](11-dom-event-listeners.md) and even [event streams](https://baconjs.github.io) this way.
