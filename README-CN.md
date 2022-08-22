# Toaster.js

`Toaster.js` 是一个基于 jQuery 的弹出提示框插件，也叫 Toast Notification。`Toaster.js` 正如它名字那样简单，它不像其他弹出框 JS 库那么臃肿，它只有非常基础的功能。它的 css 和 js 文件加起来一共不超过 5KB.

## 使用

克隆本仓库，或者直接下载仓库 `main` 分支

```
$ git clone https://github.com/BigCoke233/toaster.js.git
```

确保你引用了 jQuery，目前 `toaster.js` 需要 jQuery 的支持，但之后会开发原生 JS 版本。

```html
<link rel="stylesheet" href="toaster.css" />
<!-- ... --->
<script src="jquery.min.js"></script>
<script src="toaster.js"></script>
```

当你需要弹出一个提示框时，你只需要：

```javascript
Toaster.toast('文字内容');
```

如果你需要弹出一个错误信息，下面这个方法能把提示框变成红色：

```javascript
Toaster.error('文字内容');
```

用以上方法弹出的信息框两秒后就会自动消失，直接点击它也会让它消失；每当有新的信息框出现，上一个信息框也会消失。

如果你希望自定义某些属性，可以这样写：

```javascript
Toaster.toast('文字内容', {
    autoClose: true, //是否自动关闭提示框，默认为 true
    autoCloseDelay: 2000, //若 autoClose 为 true，则该设置生效，决定在多少毫秒之后自动关闭提示框
    color: '#C5C56A', //自定义提示框的背景色，默认为抹茶绿
    position: 'right-top', //提示框弹出方向，可选的有 right-top left-top right-bottom left-bottom center
    onClick: function(){} //定义点击提示框后的事件，默认为 undefined
})
```

---

Copyright &copy; 2022 [Eltrac](https://github.com/BigCoke233)