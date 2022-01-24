# 不要微信内置浏览器！

原因：[微信内置代理](https://x5.tencent.com/tbs/technical.html#/detail/web/1/849c02ab-8165-4e55-8628-e3ba8d8cf30e)、缓存机制烦人等，尤其是对于老安卓系统，X5内核基本没法用

## 效果

![图片](https://mapp.alicdn.com/1643022702311mdOSQSwuqKqOmhh.png)

## 使用方法

在你的 HTML 的页面 header 中添加
```html
<script src="https://timpaik.gitee.io/pages/nowechatbrowser.js"></script>
```
即可

### 高级用法

js的原理是获取当前页面的标题和URL并跳转到 `nowechatbrowser.html`,
`nowechatbrowser.html`可以接受的参数有: `url`(要跳转的URL)、`title`(跳转页面显示的标题)

例如：`https://timpaik.gitee.io/pages/nowechatbrowser?url=www.baidu.com&title=test`

就会显示URL为`www.baidu.com`, 标题是`test`

## 注意

在检测到不是微信的情况下，页面会自动跳转到目标URL

 - index.html: 测试页面
 - no.html: 跳转提示页面
 - nowechatbrowser.html: 压缩优化之后的跳转提示页面
 - nowechatbrowser.js: 自动判断是否跳转的js

## 关于微信内置浏览器

事实上，目前的TBS 5/微信内置浏览器已经能在HTML5test中获得520分以上的分数，也已经支持了绝大部分HTML5的API

所以你很可能用不到本项目（

不过，总有人会踩一脚内置浏览器的坑，希望这个项目对他们能有一些些帮助。