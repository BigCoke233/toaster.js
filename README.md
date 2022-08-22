# toaster.js

目前一些常见的信息提示框组件似乎都有些过于臃肿，如 `alertify.js` 和 `notyf.js` 等。
他们有许多自定义极强的功能，但其中有 80% 的内容你可能都不会用到，甚至还不如原生的 `alert()` 来得方便。
引用这些开源项目，尽管效果很不错，但其中没有用到的代码会大大浪费文件体积。如果你追求**轻量级**，这肯定是你不愿意看到的。
我在开发别的项目的时候正好遇到了这个问题，于是随手写下了 `toaster.js`。

## 使用

确保你引用了 jQuery，目前 `toaster.js` 需要 jQuery 的支持，但之后会开发原生 JS 版本。

分别引入 `toaster.js` 和 `toaster.css`，当你需要弹出一个提示框时，你只需要：

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

Copyright &copy; 2022 BigCoke233