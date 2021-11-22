# iframe-developing

iframe 开发示例。

## 1. iframe 内容高度自适应

关键： 动态获取 iframe 内最外层盒子的 scrollHeight 并在父页面中设置给 iframe。

```js
setInterval(() => {
			const iframeContainer = document.getElementById('iframe')
			const iframeContainerHeight = iframeContainer.contentWindow.document.getElementsByClassName('iframe-container')[0].scrollHeight  // iframe-container 为 iframe 子页面中最外层盒子的类名，这里的问题是如果直接获取 iframe html/body 的 scrollHeight 会造成手动设置后无法再自适应撑开，导致只能改变一次。
		}, 1000);
```
