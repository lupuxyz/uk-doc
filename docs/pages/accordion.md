# 手风琴

<p class="uk-text-lead">创建一个内容列表，可以通过点击标题单独地显示它的内容。</p>

## 用法

手风琴组件的组成部分包括：`uk-accordion` 属性定义的父容器，以及多个有标题和内容组成的手风琴条目。

| Class                   | Description                                                                |
|:------------------------|:---------------------------------------------------------------------------|
| `.uk-accordion-title`   | 定义手风琴条目的拨动器，并设置样式。使用 `<a>` 元素 |
| `.uk-accordion-content` | 定义每条 手风琴条目的内容部分                           |

```html
<ul uk-accordion>
    <li>
        <a class="uk-accordion-title" href="#"></a>
        <div class="uk-accordion-content"></div>
    </li>
</ul>
```

```example
<ul uk-accordion>
    <li class="uk-open">
        <a class="uk-accordion-title" href="#">Item 1</a>
        <div class="uk-accordion-content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 2</a>
        <div class="uk-accordion-content">
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor reprehenderit.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 3</a>
        <div class="uk-accordion-content">
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat proident.</p>
        </div>
    </li>
</ul>
```

***

## 无收缩 

默认情况下，所有手风琴条目都可以收缩起来。要始终保持其中一个是展开的，需要在 `uk-accordion` 属性上添加 `collapsible: false` 选项。

```html
<ul uk-accordion="collapsible: false">...</ul>
```

```example
<ul uk-accordion="collapsible: false">
    <li>
        <a class="uk-accordion-title" href="#">Item 1</a>
        <div class="uk-accordion-content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 2</a>
        <div class="uk-accordion-content">
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor reprehenderit.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 3</a>
        <div class="uk-accordion-content">
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat proident.</p>
        </div>
    </li>
</ul>
```

***

## 同时展开多项

实现同时展开多项，添加 `multiple: true` 选项到 `uk-accordion` 属性上。

```html
<ul uk-accordion="multiple: true">...</ul>
```

```example
<ul uk-accordion="multiple: true">
    <li class="uk-open">
        <a class="uk-accordion-title" href="#">Item 1</a>
        <div class="uk-accordion-content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 2</a>
        <div class="uk-accordion-content">
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor reprehenderit.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 3</a>
        <div class="uk-accordion-content">
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat proident.</p>
        </div>
    </li>
</ul>
```

***

## 设置默认展开

手动指定某些条目默认展开，给这些条目添加 `.uk-open` class 即可。同样可用于展开多个条目，首先你得确定已经把 `multiple: true` 选项添加到 `uk-accordion` 属性上了。

**Note** 此外，你还可以通过在 `uk-accordion` 属性上添加 `active: <index>` 选项来展开某个条目，例如， `active: 1` 用来显示第二个，index 索引是从0开始的。注意，这操作会覆盖掉 `uk-open` class。

```html
<ul uk-accordion>
    <li></li>
    <li class="uk-open"></li>
    <li></li>
</ul>
```

```example
<ul uk-accordion>
    <li>
        <a class="uk-accordion-title" href="#">Item 1</a>
        <div class="uk-accordion-content">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
        </div>
    </li>
    <li class="uk-open">
        <a class="uk-accordion-title" href="#">Item 2</a>
        <div class="uk-accordion-content">
            <p>Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor reprehenderit.</p>
        </div>
    </li>
    <li>
        <a class="uk-accordion-title" href="#">Item 3</a>
        <div class="uk-accordion-content">
            <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat proident.</p>
        </div>
    </li>
</ul>
```

***

## 组件选项

任意以下选项都能用于组件属性中。用分号隔开多个选项。[了解更多](javascript.md#component-configuration)

| Option        | Value   | Default | Description                                |
|:--------------|:--------|:--------|:-------------------------------------------|
| `active`      | Number  | `false` | 手动展开的元素的索引值    |
| `animation`   | Boolean | `true`  | 直接展开显示条目，或者带一个过渡动画  |
| `collapsible` | Boolean | `true`  | 允许所有条目都可以关闭              |
| `content`     | String  | `> .uk-accordion-content` | 条目内容选择器，用于指定条目的内容元素  |
| `duration`    | Number  | `200`   | 以毫秒计时的动画持续时间。        |
| `multiple`    | Boolean | `false` | 允许展开多个条目                 |
| `targets`     | String  | `> *`   | 要拨动的元素的 CSS 选择器  |
| `toggle`      | String  | `> .uk-accordion-title` | 拨动手风琴展开/收起的元素的选择器  |
| `transition`  | String  | `ease`  | 显示条目时用到的过渡效果。使用 [easing functions](https://developer.mozilla.org/en-US/docs/Web/CSS/single-transition-timing-function#Keywords_for_common_timing-functions) 中的关键词。 |

***

## JavaScript

了解更多关于  [JavaScript 组件](javascript.md#programmatic-use).

### 初始化

```js
UIkit.accordion(element, options);
```

### 事件

以下事件将在此组件相关元素上触发：

| Name         | Description                                                              |
|:-------------|:-------------------------------------------------------------------------|
| `beforeshow` | 在条目被显示前触发。可以通过返回 `false` 来阻止显示。 |
| `show`       | 在条目被显示后触发。                                           |
| `shown`      | 条目显示的动画完成后触发               |
| `beforehide` | 在条目被隐藏前触发。可以通过返回 `false` 来阻止显示   |
| `hide`       | 条目的隐藏动画开始后触发               |
| `hidden`     | 在条目被隐藏后触发。                                           |

### 方法

以下方法可用于此组件：

#### Toggle

```js
UIkit.accordion(element).toggle(index, animate);
```

拨动内容条目显示。

| Name      | Type                  | Default | Description                                  |
|:----------|:----------------------|:--------|:---------------------------------------------|
| `index`   | String, Integer, Node | 0       | 要拨动手风琴条目索引值，从0开始。    |
| `animate` | Boolean               | true    | 传入 false 可以关闭展开时的动画。  |
