---
category: API
title: 模板渲染函数
order: 5
---

AcyOrt 提供一个 `helper` 方法，除了能够访问内置的辅助渲染函数外，还可以注册一些自定义的函数

内置函数可以查看 [helper](/docs/helper/) 说明

**注册函数**

```js
// 注册一个自定义函数 `_test`
acyort.helper.register('_test', function test() {
  return `<p>${acyort.version}</p>`
})
```

```html
<!-- 模板页面使用 -->
<div>{{ _test() }}</div>
```