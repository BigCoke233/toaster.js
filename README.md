# Toaster.js

> 这里有一个[简体中文版本](README-CN.md)的说明文档

`Toaster.js` is a toast notification library depending on jQuery. As the name it has, `toaster.js` only include a few basic functions unlike other well-designed but overweight libraries. The total size of its CSS and JavaScript file is even less than 5KB before compressing.

## Usage

Clone or just grab `toaster.js` and `toaster.css` in the `main` branch.

```git
$ git clone https://github.com/BigCoke233/toaster.js.git
```

Make sure you include jQuery and toaster.

```html
<link rel="stylesheet" href="toaster.css" />
<!-- ... --->
<script src="jquery.min.js"></script>
<script src="toaster.js"></script>
```

Whenever you feel like you need a notification, just do this.

```javascript
Toaster.toast('text');
```

If you can also send a warning with a red background like this.

```javascript
Toaster.error('warning');
```

Toasts sent by these methods above will automatically vanish after 2 seconds unless you click on it.

## API

You can set some more options like this when creating a toast.

```javascript
Toaster.toast('text', {
    autoClose: true,
    autoCloseDelay: 2000,
    color: '#C5C56A',
    position: 'right-top',
    onClick: function(){}
})
```

| API Name | Default | Explanation |
| :--- | :--- | :--- |
| `autoClose` |  `true` | Whether a toast dismiss itself |
| `autoCloseDelay` | `2000` | After how long a toast automatically dismiss |
| `color` | `#C5C56A` | The background color of a toast |
| `position` | `right-top` | At which position a toast will appear. Options: `right-top`, `right-bottom`, `left-top`, `left-bottom`, `center` |
| `onClick` | `function(){}` | The events on clicking a toast |

---

Copyright &copy; 2022 [Eltrac](https://github.com/BigCoke233)
