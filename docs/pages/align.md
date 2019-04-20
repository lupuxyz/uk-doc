# 对齐

<p class="uk-text-lead">基于视口尺寸，控制行内元素的对齐。</p>

## 用法

要使文本与图片或其他元素对齐，并带有一定的间距，需要添加下面这些 class中的一个：

| Class              | Description                                                         |
|:-------------------|:--------------------------------------------------------------------|
| `.uk-align-left`   | 将元素浮动到左侧并创建右侧和底部的margin |
| `.uk-align-right`  | 将元素浮动到右侧并创建左侧和底部的margin |
| `.uk-align-center` | 居中元素，并创建底部margin                      |

```html
<img class="uk-align-left" src="" alt="">
```

```example
<div class="uk-panel">
    <img class="uk-align-left uk-margin-remove-adjacent" src="images/light.jpg" width="225" height="150" alt="Example image">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
</div>
```

***

## 响应式

UIkit 提供了一系列响应式对齐class。通常，它们与一般的对齐class效果一样，但是它们拥有的后缀表示它们会根据不同的断点产生效果。

| Class                                        | Description                                        |
|:---------------------------------------------|:---------------------------------------------------|
| `.uk-align-left@s`<br> `.uk-align-right@s`   | 仅作用于宽度在 _640px_ 以上的设备 |
| `.uk-align-left@m`<br> `.uk-align-right@m`   | 仅作用于宽度在 _960px_ 以上的设备  |
| `.uk-align-left@l`<br> `.uk-align-right@l`   | 仅作用于宽度在 _1200px_ 以上的设备 |
| `.uk-align-left@xl`<br> `.uk-align-right@xl` | 仅作用于宽度在 _1600px_ 以上的设备 |

```html
<img class="uk-align-center uk-align-right@m" src="" alt="">
```

```example
<div class="uk-panel">
    <img class="uk-align-center uk-align-right@m uk-margin-remove-adjacent"  src="images/light.jpg" width="225" height="150" alt="Example image">
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
    <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
</div>
```
