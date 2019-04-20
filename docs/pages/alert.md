# 提示框

<p class="uk-text-lead">显示成功、警告、错误类信息。 </p>

## 用法 

在块级元素上添加 `uk-alert` 属性即可使用。

```html
<div uk-alert></div>
```

```example
<div uk-alert>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</div>
```

***

## 关闭按钮

提示框内部的 `<button>` 或 `<a>` 元素上添加 `.uk-alert-close` class，即可创建一个关闭按钮，并启用其功能。再添加一个 [关闭组件](close.md) 中的 `uk-close` 属性来实现关闭图标。

```html
<div uk-alert>
    <a class="uk-alert-close" uk-close></a>
</div>
```

```example
<div uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <h3>Notice</h3>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
</div>
```

***

## 样式修改

添加以下样式修改 class 使其呈现不同的外观风格：

| Class               | Description                               |
|:--------------------|:------------------------------------------|
| `.uk-alert-primary` | 为信息添加主色调样式     |
| `.uk-alert-success` | 表示成功或积极的信息  |
| `.uk-alert-warning` | 表示包含警告的信息 |
| `.uk-alert-danger`  | 表示重要或错误的信息  |

```example
<div class="uk-alert-primary" uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>
</div>

<div class="uk-alert-success" uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>
</div>

<div class="uk-alert-warning" uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>
</div>

<div class="uk-alert-danger" uk-alert>
    <a class="uk-alert-close" uk-close></a>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.</p>
</div>
```

***

## 组件选项

任意以下选项都能用于组件属性中。用分号隔开多个选项。[了解更多](javascript.md#component-configuration)

| Option      | Value           | Default           | Description                                              |
|:------------|:----------------|:------------------|:---------------------------------------------------------|
| `animation` | Boolean, String | `true`            | 淡出效果，或者使用[动画组件](animation.md). |
| `duration`  | Number          | `150`             | 以毫秒计时的动画持续时间                     |
| `sel-close` | CSS selector    | `.uk-alert-close` | 触发关闭的元素                               |

`animation` 是 _主要_ 选项，作为属性中的唯一选项时，可以省略其名称：

```html
<span uk-toggle=".my-class"></span>
```

***

## JavaScript

了解更多关于  [JavaScript 组件](javascript.md#programmatic-use).

### 初始化

```js
UIkit.alert(element, options);
```

### 事件

以下事件将在此组件相关元素上触发：

| Name         | Description                                                              |
|:-------------|:-------------------------------------------------------------------------|
| `beforehide` | 在条目被隐藏前触发。可以通过返回 `false` 来阻止显示。 |
| `hide`       | 在条目被隐藏后触发。                                          |

### 方法

以下方法可用于此组件：

#### Close

```js
UIkit.alert(element).close();
```

关闭并移除提示框。
