# Tooltip

<p class="uk-text-lead">Easily create a nice looking tooltip.</p>

## 用法

To apply this component, add the `uk-tooltip` attribute to an element. You also need to add the `title: TEXT` option to the attribute, whose value will represent your tooltip's text.

```html
<div uk-tooltip="title: Hello World"></div>
```

If `title` is the only option in the attribute value, you can also use `uk-tooltip="TEXT"`

```html
<div uk-tooltip="Hello World"></div>
```

```example
<button class="uk-button uk-button-default" uk-tooltip="Hello World">Hover</button>
```

***

## Alignment

Add one of the following options to the `uk-tooltip` attribute to adjust the tooltip's alignment.

```html
<button uk-tooltip="title: Hello World; pos: top-left"></button>
```

| Attribute           | Description                             |
|:--------------------|:----------------------------------------|
| `pos: top`          | Aligns the tooltip to the top.          |
| `pos: top-left`     | Aligns the tooltip to the top left.     |
| `pos: top-right`    | Aligns the tooltip to the top right.    |
| `pos: bottom`       | Aligns the tooltip to the bottom.       |
| `pos: bottom-left`  | Aligns the tooltip to the bottom left.  |
| `pos: bottom-right` | Aligns the tooltip to the bottom right. |
| `pos: left`         | Aligns the tooltip to the left.         |
| `pos: right`        | Aligns the tooltip to the right.        |

```example
<p uk-margin>
    <button class="uk-button uk-button-default" uk-tooltip="Hello World">Top</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: top-left">Top Left</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: top-right">Top Right</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: bottom">Bottom</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: bottom-left">Bottom Left</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: bottom-right">Bottom Right</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: left">Left</button>
    <button class="uk-button uk-button-default" uk-tooltip="title: Hello World; pos: right">Right</button>
</p>
```

***

## Delay

If you want the tooltip to appear with a little delay, just add the `delay` option to the `uk-tooltip` attribute with your value in milliseconds.

```html
<div uk-tooltip="title: Hello World; delay: 500"></div>
```

```example
<button class="uk-button uk-button-default" uk-tooltip="title: Hello World; delay: 500">Hover</button>
```

***

## 组件选项

任意以下选项都能用于组件属性中。用分号隔开多个选项。[了解更多](javascript.md#component-configuration)

| Option      | Value  | Default                 | Description                                                                       |
|:------------|:-------|:------------------------|:----------------------------------------------------------------------------------|
| `title`     | String | ``                      | Tooltip text.                                                                 |
| `pos`       | String | `top`                   | Tooltip position.                                                                 |
| `offset`    | Number | `false`                 | Tooltip offset.                                                        |
| `animation` | String | `uk-animation-scale-up` | The space separated names of animations to use. Comma separate for animation out. |
| `duration`  | Number | `100`                   | The animation duration.                                                           |
| `delay`     | Number | `0`                     | The show delay.                                                                   |
| `cls`       | String | `uk-active`             | The active class.                                                                 |

`title` is the _Primary_ option and its key may be omitted, if it's the only option in the attribute value.

```html
<span uk-tooltip="Hello World"></span>
```

***

## JavaScript

了解更多关于  [JavaScript 组件](javascript.md#programmatic-use).

### 初始化

```js
UIkit.tooltip(element, options);
```

### 事件

以下事件将在由此组件注入的元素上触发：

| Name         | Description                                                              |
|:-------------|:-------------------------------------------------------------------------|
| `beforeshow` | Fires before an item is shown. Can prevent showing by returning `false`. |
| `show`       | Fires after an item is shown.                                            |
| `shown`      | Fires after the item's show animation has completed.                     |
| `beforehide` | Fires before an item is hidden. Can prevent hiding by returning `false`. |
| `hide`       | Fires after an item's hide animation has started.                        |
| `hidden`     | Fires after an item is hidden.                                           |

#### Example

```javascript
UIkit.util.on(document, 'show', '.uk-tooltip.uk-active', function() {
  // do something
});
```

### 方法

以下方法可用于此组件：

#### Show

```js
UIkit.tooltip(element).show();
```

Shows the Tooltip.

#### Hide

```js
UIkit.tooltip(element).hide();
```

Hides the Tooltip.
