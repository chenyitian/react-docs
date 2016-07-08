# DOM Event Listeners in a Component

> Note:
>
> This entry shows how to attach DOM events not provided by React ([check here for more info](../docs/ref-05-events.md)). This is good for integrations with other libraries such as jQuery.

Try to resize the window:

```javascript
var Box = React.createClass({
  getInitialState: function() {
    return {windowWidth: window.innerWidth};
  },

  handleResize: function(e) {
    this.setState({windowWidth: window.innerWidth});
  },

  componentDidMount: function() {
    window.addEventListener('resize', this.handleResize);
  },

  componentWillUnmount: function() {
    window.removeEventListener('resize', this.handleResize);
  },

  render: function() {
    return <div>Current window width: {this.state.windowWidth}</div>;
  }
});

ReactDOM.render(<Box />, mountNode);
```

`componentDidMount` is called after the component is mounted and has a DOM representation. This is often a place where you would attach generic DOM events.

Notice that the event callback is bound to the react component and not the original element. React automatically binds methods to the current component instance for you through a process of [autobinding](../docs/03-interactivity-and-dynamic-uis.md#under-the-hood-autobinding-and-event-delegation).
