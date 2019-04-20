# Scroll

<p class="uk-text-lead">Scroll smoothly when jumping to different sections on a page.</p>

## 用法

Simply add the `uk-scroll` attribute to any page-internal link that contains a URL fragment to add the smooth scrolling behavior.

```html
<a href="#my-id" uk-scroll></a>
```

```example
<a class="uk-button uk-button-primary" href="#target" uk-scroll>Scroll down</a>
```

***

## Callback after scroll

To receive a callback when scrolling has completed, you can listen to the `scrolled` event on the link element that triggered the scrolling.

```html
<a id="js-scroll-trigger" href="#my-id" uk-scroll></a>
```

```js
UIkit.util.on('#scroll-trigger', 'scrolled', function () {
    alert('Done.');
});
```

```example
<a id="js-scroll-trigger" class="uk-button uk-button-primary" href="#target" uk-scroll>Down with callback</a>

<script>
    UIkit.util.on('#js-scroll-trigger', 'scrolled', function () {
        alert('Done.');
    });
</script>
```

***

## 组件选项

任意以下选项都能用于组件属性中。用分号隔开多个选项。[了解更多](javascript.md#component-configuration)

| Option     | Value  | Default | Description                         |
|:-----------|:-------|:--------|:------------------------------------|
| `duration` | Number | `1000`  | Animation duration in milliseconds. |
| `offset`   | Number | `0`     | Pixel offset added to scroll top.   |

## JavaScript

了解更多关于  [JavaScript 组件](javascript.md#programmatic-use).

### 初始化

```js
UIkit.scroll(element, options);
```

<div style="height: 2000px;"></div>

<a id="target" class="uk-button uk-button-primary" href="#top" uk-scroll>Scroll up</a>

### 事件

以下事件将在此组件相关元素上触发：

| Name           | Description                                                             |
|:---------------|:------------------------------------------------------------------------|
| `beforescroll` | Fires before scroll begins. Can prevent scrolling by returning `false`. |
| `scrolled`     | Fires after scrolling is finished.                                      |


### 方法

以下方法可用于此组件：

#### ScrollTo

```js
UIkit.scroll(element).scrollTo(el);
```

Scroll to the given element.

| Name | Type           | Default   | Description               |
|:-----|:---------------|:----------|:--------------------------|
| `el` | Node, Selector | undefined | The element to scroll to. |
