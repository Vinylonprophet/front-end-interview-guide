# HTML面试题

## 标签

### 1. 简述一下src与href的区别？

`src` 属性：

- `src` 属性（source）通常用于表示资源的位置，例如图片、音频、视频等。
- 它是一些标签的属性，比如 `<img>`、`<script>`、`<iframe>` 等，用于指定要嵌入的外部资源的地址。
- 例如，`<img src="image.jpg">` 表示要加载图片 `image.jpg`，`<script src="script.js"></script>` 表示要加载脚本文件 `script.js`。
- `src` 属性用于替换当前元素的内容。

`href` 属性：

- `href` 属性（hypertext reference）用于表示超链接的目标地址，通常用于 `<a>`、`<link>`、`<area>` 等标签中。
- 它指定了要链接到的文档的 URL 地址。
- 例如，`<a href="https://www.example.com">Link</a>` 表示创建了一个指向 `https://www.example.com` 的超链接。
- `href` 属性用于指定一个超链接的目标，点击链接会跳转到指定的 URL 地址。

区别总结：

- `src` 属性用于嵌入外部资源，例如图片、脚本、框架等，替换当前元素的内容。
- `href` 属性用于指定超链接的目标地址，用于创建超链接，点击链接会跳转到指定的 URL 地址。

简单来说，`src` 用于引入资源，`href` 用于指定超链接。

