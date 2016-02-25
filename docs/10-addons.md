# 插件

React插件是一系列的用来构建React app的有用模块。 **这些应该被认为是实验性的** 并趋向于比core变动更频繁。

- [`TransitionGroup` 和 `CSSTransitionGroup`](10.1-animation.md), 用来处理通常不能简单实现的动画和转换，比如在组件移除之前。
- [`LinkedStateMixin`](10.2-form-input-binding-sugar.md), 简化用户的表单输入数据与组件状态的协调。
- [`cloneWithProps`](10.5-clone-with-props.md), 创建React组件的浅拷贝并改变它们的props。
- [`createFragment`](10.6-create-fragment.md), 创建一组外键的子级。
- [`update`](10.7-update.md), 一个使不可变数据在JavaScript里更易处理的辅助函数。
- [`PureRenderMixin`](10.8-pure-render-mixin.md), 一个特定情况下的性能优化器。
- [`shallowCompare`](10.10-shallow-compare.md), 一个辅助函数，用来对 props 和 state在组件里 执行浅比较 以决定一个组件是否应该更新。

下面的插件只存在开发版(未压缩)React中：

- [`TestUtils`](10.4-test-utils.md), 用于写测试用例的简单的辅助工具（仅存在于未压缩版本）。
- [`Perf`](10.9-perf.md), 用于测量性能并给你提示哪里可以优化。

要获取插件，单独从npm安装他们(例如 `npm install react-addons-pure-render-mixin`).我们不支持使用插件如果你没有用npm.
