# [React](https://facebook.github.io/react/)
React是用于构建用户界面的JAVASCRIPT库。

* **仅仅是UI：**许多人使用React作为MVC架构的V层。尽管React并没有假设过你的其余技术栈，但它仍可以作为一个小特征轻易地在已有项目中使用。
* **虚拟DOM：**React为了更高超的性能而使用虚拟DOM作为其不同的实现。它同时也可以由服务端Node.js渲染——而不需要过重的浏览器DOM支持。
* **数据流：**React实现了单向响应的数据流，从而减少了重复代码，这也是它为什么比传统数据绑定更简单。

## 致谢

We'd like to thank all of our contributors:

<div class="three-column">
  {% for author_col in site.data.acknowledgements %}
  <ul>
    {% for author in author_col %}
    <li>{{ author }}</li>
    {% endfor %}
  </ul>
  {% endfor %}
</div>

In addition, we're grateful to
 - [Jeff Barczewski](https://github.com/jeffbski) for allowing us to use the [react](https://www.npmjs.com/package/react) package name on npm.
 - [Christopher Aue](http://christopheraue.net/) for letting us use the [reactjs.com](http://reactjs.com/) domain name and the [@reactjs](https://twitter.com/reactjs) username on Twitter.
 - [ProjectMoon](https://github.com/ProjectMoon) for letting us use the [flux](https://www.npmjs.com/package/flux) package name on npm.
 - Shane Anderson for allowing us to use the [react](https://github.com/react) org on GitHub.