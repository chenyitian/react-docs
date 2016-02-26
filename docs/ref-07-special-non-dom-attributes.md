# 特殊的 Non-DOM Attributes

和 [DOM 的不同之处](ref-06-dom-differences.md)相比，React 提供了一些不存在于 DOM 的 attributes。

- `key`：一个可选的。独特的标识。当你的组件穿梭于 `render` 的 pass，它也许会因为 diff 算法被摧毁和重建。赋予它一个持久的 key 保证这个 component 可达。详见[这里](04-multiple-components.md#dynamic-children)。
- `ref`：见[这里](08.1-more-about-refs.md)。
- `dangerouslySetInnerHTML`：提供了直接插入 raw HTML 的能力，主要是为了与操纵 DOM 字符串的库协作。详见[这里](../tips/19-dangerously-set-inner-html.md)。
