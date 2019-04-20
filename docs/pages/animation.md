# 动画

<p class="uk-text-lead">用在网页上的一系列流畅的动画。 </p>

## 用法

在任意元素上 添加 `.uk-animation-*` class。动画在 Class 被添加时就会显示，所以通常会在页面加载时即刻生效。想要实现在其他情况下显示动画，例如在元素进入视口时，你需要使用 JavaScript 来添加动画的 class —— 比如使用 [滚动监听组件](scrollspy.md) 。这是 UIkit 的多数组件使用动画的方式。所有动画本身都是用 CSS 实现的，不需要使用 JavaScript来播放。

| Class                                                   | Description                                          |
|:--------------------------------------------------------|:-----------------------------------------------------|
| `.uk-animation-fade`                                    | 元素的淡入效果                                |
| `.uk-animation-scale-up`<br> `.uk-animation-scale-down` | 元素的缩放效果          |
| `.uk-animation-slide-top`<br> `.uk-animation-slide-bottom`  `.uk-animation-slide-left`<br> `.uk-animation-slide-right` | 元素基于它的高度或宽度从顶部、底部、左侧或右侧淡入并滑入。 |
| `.uk-animation-slide-top-small`<br> `.uk-animation-slide-bottom-small`   `.uk-animation-slide-left-small`<br> `.uk-animation-slide-right-small` | 元素从顶部、底部、左侧或右侧淡入并滑入，并带有固定像素值的较小距离。 |
| `.uk-animation-slide-top-medium`<br> `.uk-animation-slide-bottom-medium`  `.uk-animation-slide-left-medium`<br> `.uk-animation-slide-right-medium` | 元素从顶部、底部、左侧或右侧淡入并滑入，并带有固定像素值的中等距离。 |
| `.uk-animation-kenburns`                                | 元素不带淡入效果缓慢地缩放 |
| `.uk-animation-shake`                                   | 元素抖动                                  |
| `.uk-animation-stroke`                                  | SVG 的笔触绘图效果                   |

To toggle an animation on hover or focus, add the `.uk-animation-toggle` class to a parent element. Also add `tabindex="0"` to make the animation focusable through keyboard navigation and on touch devices.

```html
<div class="uk-animation-toggle" tabindex="0">
    <div class="uk-animation-fade"></div>
</div>
```

```example
<div class="uk-child-width-1-2 uk-child-width-1-4@s uk-grid-match" uk-grid>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-fade">
            <p class="uk-text-center">Fade</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-up">
            <p class="uk-text-center">Scale Up</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-down">
            <p class="uk-text-center">Scale Down</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-shake">
            <p class="uk-text-center">Shake</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-left">
            <p class="uk-text-center">Left</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-top">
            <p class="uk-text-center">Top</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-bottom">
            <p class="uk-text-center">Bottom</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-right">
            <p class="uk-text-center">Right</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-left-small">
            <p class="uk-text-center">Left Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-top-small">
            <p class="uk-text-center">Top Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-bottom-small">
            <p class="uk-text-center">Bottom Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-right-small">
            <p class="uk-text-center">Right Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-left-medium">
            <p class="uk-text-center">Left Medium</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-top-medium">
            <p class="uk-text-center">Top Medium</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-bottom-medium">
            <p class="uk-text-center">Bottom Medium</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-right-medium">
            <p class="uk-text-center">Right Medium</p>
        </div>
    </div>
</div>
```

***

## 反向动画

默认地，所有动画都是元素出现的效果。要把动画反向，比如元素消失的效果，添加  `.uk-animation-reverse` class 。

```html
<div class="uk-animation-fade uk-animation-reverse"></div>
```

```example
<div class="uk-child-width-1-2 uk-child-width-1-4@s uk-grid-match" uk-grid>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-fade uk-animation-reverse">
            <p class="uk-text-center">Fade</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-up uk-animation-reverse">
            <p class="uk-text-center">Scale Up</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-down uk-animation-reverse">
            <p class="uk-text-center">Scale Down</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-shake uk-animation-reverse">
            <p class="uk-text-center">Shake</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-left uk-animation-reverse">
            <p class="uk-text-center">Left</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-top uk-animation-reverse">
            <p class="uk-text-center">Top</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-bottom uk-animation-reverse">
            <p class="uk-text-center">Bottom</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-right uk-animation-reverse">
            <p class="uk-text-center">Right</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-left-small uk-animation-reverse">
            <p class="uk-text-center">Left Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-top-small uk-animation-reverse">
            <p class="uk-text-center">Top Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-bottom-small uk-animation-reverse">
            <p class="uk-text-center">Bottom Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-right-small uk-animation-reverse">
            <p class="uk-text-center">Right Small</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-left-medium uk-animation-reverse">
            <p class="uk-text-center">Left Medium</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-top-medium uk-animation-reverse">
            <p class="uk-text-center">Top Medium</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-bottom-medium uk-animation-reverse">
            <p class="uk-text-center">Bottom Medium</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-slide-right-medium uk-animation-reverse">
            <p class="uk-text-center">Right Medium</p>
        </div>
    </div>
</div>
```

***

## 快速动画

要以更快的速度播放动画，添加 `.uk-animation-fast` class 到元素。

```html
<div class="uk-animation-fade uk-animation-fast"></div>
```


```example
<div class="uk-width-1-3@s">
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-fast uk-animation-fade">
            <p class="uk-text-center">Fade</p>
        </div>
    </div>
</div>
```

***

## 动画起点

默认情况下，缩放动画的源头是中间。修改这个行为，添加一个[实用效果组件](utility.md#transform-origin) 中的 `.uk-transform-origin-*` class。

```html
<div class="uk-animation-scale-up uk-transform-origin-bottom-right"></div>
```

```example
<div class="uk-child-width-1-3@s" uk-grid>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-up uk-transform-origin-bottom-right">
            <p class="uk-text-center">Bottom Right</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-up uk-transform-origin-top-center">
            <p class="uk-text-center">Top Center</p>
        </div>
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <div class="uk-card uk-card-default uk-card-body uk-animation-scale-up uk-transform-origin-bottom-center">
            <p class="uk-text-center">Bottom Center</p>
        </div>
    </div>
</div>
```

***

## Ken Burns

添加简单的 Ken Burns 效果，需要为图片添加 `.uk-animation-kenburns` class。还可以使用  `.uk-animation-reverse` 或 `.uk-transform-origin-*` classe 来修改效果。

```html
<img class="uk-animation-kenburns" src="" alt="">
```

By default the animation starts on page load. In this example we used the [Scrollspy](scrollspy.md) component, to toggle the effect when the image enters the view.

```example
<div class="uk-child-width-1-2@s uk-grid-small" uk-grid>
    <div>
        <div class="uk-overflow-hidden">
            <img src="images/dark.jpg" alt="Example image" uk-scrollspy="cls: uk-animation-kenburns; repeat: true">
        </div>
    </div>
    <div>
        <div class="uk-overflow-hidden">
            <img src="images/dark.jpg" alt="Example image" class="uk-animation-reverse uk-transform-origin-top-right" uk-scrollspy="cls: uk-animation-kenburns; repeat: true">
        </div>
    </div>
</div>
```

***

## SVG Strokes

动画组件可以用于 SVG 绘制动画。这个效果看起来就像在你眼前绘制 SVG 一样。SVG 图片是以行内 SVG 的形式注入到标签内的。可以手动操作，或者使用 [SVG 组件](svg.md)。

下面的例子为你展示如何手动添加行内 SVG。The following example shows how to add the inline SVG manually. Since you have to know the exact length of the stroke, UIkit requires you to set the length in the custom property `--uk-animation-stroke`. In this example the stroke length is `46`.

```html
<svg class="uk-animation-stroke" style="--uk-animation-stroke: 46;" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
    <path fill="none" stroke="#000" stroke-width="1" d=""/>
</svg>
```

A much easier way is to use the [SVG component](svg.md) by adding `uk-svg="animation-stroke: true"` to the image element. It will calculate the stroke length and add the `--uk-animation-stroke` custom property automatically.

```html
<img src="" uk-svg="animation-stroke: true">
```

```example
<div class="uk-child-width-1-2@m uk-text-center" uk-grid>
    <div class="uk-animation-toggle" tabindex="0">
        <img class="uk-animation-stroke" width="400" height="400" src="images/strokes.svg" alt="" uk-svg="stroke-animation: true">
    </div>
    <div class="uk-animation-toggle" tabindex="0">
        <img class="uk-animation-stroke uk-animation-reverse" width="400" height="400" src="images/strokes.svg" alt="" uk-svg="stroke-animation: true">
    </div>
</div>
```