# HTML 中的 JavaScript

script

- 使用方法：

  - 行内 js
  - 外部文件

- 位置：

  - head 里
  - body 的最后

defer ： 立即下载，但是执行推迟，（通常）顺序执行，（通常）在 DOMContentLoaded 时间之前执行

async：立即下载，不保证顺序执行

动态加载： dom 添加 script，想要预加载，可以配合 `<link rel=“preload” href=“gibberish.js” >` 在 head 中使用

2.2 行内代码 vs 外部文件

    * 可维护性
    * 缓存： 两个页面引用同一个文件，该文件只需下载一次
    * 适应性

noscript

    * 浏览器不支持脚本
    * 浏览器对脚本禁用
