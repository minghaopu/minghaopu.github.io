---
title: CSS Layout 1 - Flexbox
description: CSS Flexbox Layout Introduction
categories:
 - css
 - layout
tags:
 - css
 - layout
---

# Flex Layout

## Definition:

>Flexible boxes, or flexbox, is a new layout mode in CSS3.
>
>Use of flexbox ensures that elements behave predictably when the page layout must accommodate different screen sizes and different display devices.
>
>For many applications, the flexible box model provides an improvement over the block model in that it does not use floats, nor do the flex container's margins collapse with the margins of its contents.

## Cross-browser

[Cross-browser](http://caniuse.com/#search=flex)

## How to use

Inorder to use this new feathure, you only need to set `display` attribute of the element to `flex`. For example: set element in middle

<div id='sample'>
  <style>
  #sample .outer {
    display: flex;
    width: 100%;
    height: 300px;
    border: 1px solid black;
    align-items:center;
    justify-content:center;
  }
  #sample .inner {
    width: 50%;
    height: 50%;
    background-color:#ccc;
    text-align:center
  }
  </style>
  <div class="outer">
    outer
    <div class="inner">
    inner
    </div>
  </div>
</div>
<br/>

html code
{% highlight html linenos %}
<style>
.outer {
  display: flex;
  width: 100%;
  height: 300px;
  border: 1px solid black;
  align-items: center;
  justify-content: center;
}
.inner {
  width: 50%;
  height: 50%;
  background-color: #999;
  text-align: center
}
</style>
<div class="outer">
  outer
  <div class="inner">
  inner
  </div>
</div>
{% endhighlight%}

## Related Term

![Related Term](https://developer.mozilla.org/files/3739/flex_terms.png)

# Attributions of Parent

## Introduction

1. flex-direction: determines the direction of children on main axis;
2. flex-wrap: determines whether flex items should be wrapped;
3. flex-flow: combination of `flex-wrap` and `flex-direction`;
4. justify-content: determines the layout of children on main axis;
5. align-items: determines the layourt of children on cross axis;
6. align-content: determines the space between and around content along cross axis;


## flex-drection

<!-- row -->
<div id='row'>
  <style>
    #row {
      margin: 0.3rem;
    }
    #row .outer {
    display: flex;
    width: 100%;
    height: 100px;
    border: 1px solid black;
    flex-direction: row;
  }
  #row .inner {
    width: 20%;
    height: 50%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    <div>row</div>
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>

<!-- row-reverse -->
<div id='row-reverse'>
  <style>
  #row-reverse {
    margin: 0.3rem;
  }
  #row-reverse .outer {
    display: flex;
    width: 100%;
    height: 100px;
    border: 1px solid black;
    flex-direction: row-reverse;
  }
  #row-reverse .inner {
    width: 20%;
    height: 50%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    <p>row-reverse</p>
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>
<!-- column -->
<div id='column'>
  <style>
  #column {
    margin: 0.3rem;
  }
  #column .outer {
    display: flex;
    width: 100%;
    height: 200px;
    border: 1px solid black;
    flex-direction: column;
  }
  #column .inner {
    width: 20%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    column
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>
<!-- column reverse -->
<div id='column-reverse'>
  <style>
  #column-reverse {
    margin: 0.3rem;
  }
  #column-reverse .outer {
    display: flex;
    width: 100%;
    height: 200px;
    border: 1px solid black;
    flex-direction: column-reverse;
  }
  #column-reverse .inner {
    width: 20%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    column-reverse
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>
<br/>

## flex-wrap
<!-- no wrap -->
<div id='no-wrap'>
  <style>
  #no-wrap {
    margin: 0.3rem;
  }
  #no-wrap .outer {
    display: flex;
    width: 300px;
    height: 100px;
    border: 1px solid black;
    flex-wrap: nowrap;
  }
  #no-wrap .inner {
    min-width: 100px;
    height: 30px;
    margin: 10px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    <p>no wrap</p>
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>

<!-- wrap -->
<div id='wrap'>
  <style>
  #wrap {
    margin: 0.3rem;
  }
  #wrap .outer {
    display: flex;
    width: 300px;
    height: 100px;
    border: 1px solid black;
    flex-wrap: wrap;
  }
  #wrap .inner {
    min-width: 70px;
    height: 30px;
    margin: 10px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    <p>wrap</p>
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>

<!-- wrap reverse -->
<div id='wrap-reverse'>
  <style>
  #wrap-reverse {
    margin: 0.3rem;
  }
  #wrap-reverse .outer {
    display: flex;
    width: 300px;
    height: 100px;
    border: 1px solid black;
    flex-wrap: wrap-reverse;
  }
  #wrap-reverse .inner {
    min-width: 70px;
    height: 30px;
    margin: 10px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  <div class="outer">
    <p>wrap-reverse</p>
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>

## justify-content

<!-- flex-start -->
<div id='flex-start'>
  <style>
  #flex-start {
    margin: 0.3rem;
  }
  #flex-start .outer {
    display: flex;
    width: 100%;
    height: 60px;
    border: 1px solid black;
    justify-content: flex-start
  }
  #flex-start .inner {
    width: 20%;
    height: 30px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  flex-start
  <div class="outer">
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>

<!-- flex-end -->
<div id='flex-end'>
  <style>
  #flex-end {
    margin: 0.3rem;
  }
  #flex-end .outer {
    display: flex;
    width: 100%;
    height: 60px;
    border: 1px solid black;
    justify-content: flex-end
  }
  #flex-end .inner {
    width: 20%;
    height: 30px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  flex-end
  <div class="outer">
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
    <div class="inner">4</div>
  </div>
</div>

<!-- center -->
<div id='center'>
  <style>
  #center {
    margin: 0.3rem;
  }
  #center .outer {
    display: flex;
    width: 100%;
    height: 60px;
    border: 1px solid black;
    justify-content: center;
  }
  #center .inner {
    width: 20%;
    height: 30px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  center
  <div class="outer">
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
  </div>
</div>

<!-- space-between -->
<div id='space-between'>
  <style>
  #space-between {
    margin: 0.3rem;
  }
  #space-between .outer {
    display: flex;
    width: 100%;
    height: 60px;
    border: 1px solid black;
    justify-content: space-between;
  }
  #space-between .inner {
    width: 20%;
    height: 30px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  space-between
  <div class="outer">
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
  </div>
</div>

<!-- space-around -->
<div id='space-around'>
  <style>
  #space-around {
    margin: 0.3rem;
  }
  #space-around .outer {
    display: flex;
    width: 100%;
    height: 60px;
    border: 1px solid black;
    justify-content: space-around;
  }
  #space-around .inner {
    width: 20%;
    height: 30px;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  space-around
  <div class="outer">
    <div class="inner">1</div>
    <div class="inner">2</div>
    <div class="inner">3</div>
  </div>
</div>

## align-item

<!-- flex-start -->
<div id='align-item-flex-start'>
  <style>
  #align-item-flex-start {
    margin: 0.3rem;
  }
  #align-item-flex-start .outer {
    display: flex;
    width: 100%;
    height: 150px;
    border: 1px solid black;
    align-items: flex-start
  }
  #align-item-flex-start .inner {
    width: 20%;
    border: 1px solid black;
    margin: 0.3rem;
    background-color:#ccc;
  }
  .inner.item1 {
    height: 20px !important;
  }
  .inner.item2 {
    height: 90px !important;
  }
  .inner.item3 {
    height: 40px !important;
  }
  .inner.item4 {
    height: 70px !important;
  }
  </style>
  flex-start
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
  </div>
</div>

<!-- flex-end -->
<div id='align-item-flex-end'>
  <style>
  #align-item-flex-end {
    margin: 0.3rem;
  }
  #align-item-flex-end .outer {
    display: flex;
    width: 100%;
    height: 150px;
    border: 1px solid black;
    align-items: flex-end
  }
  #align-item-flex-end .inner {
    width: 20%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  flex-end
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
  </div>
</div>

<!-- center -->
<div id='align-item-center'>
  <style>
  #align-item-center {
    margin: 0.3rem;
  }
  #align-item-center .outer {
    display: flex;
    width: 100%;
    height: 150px;
    border: 1px solid black;
    align-items: center;
  }
  #align-item-center .inner {
    width: 20%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  center
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
  </div>
</div>

<!-- align-item-baseline -->
<div id='align-item-baseline'>
  <style>
  #align-item-baseline {
    margin: 0.3rem;
  }
  #align-item-baseline .outer {
    display: flex;
    width: 100%;
    height: 150px;
    border: 1px solid black;
    align-items: baseline;
  }
  #align-item-baseline .inner {
    width: 20%;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  #align-item-baseline .inner.item1 {
    font-size: 12px;
  }
  #align-item-baseline .inner.item2 {
    font-size: 50px;
  }
  #align-item-baseline .inner.item3 {
    font-size: 20px;
  }
  #align-item-baseline .inner.item4 {
    font-size: 40px;
  }
  </style>
  baseline
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
  </div>
</div>

<!-- align-item-stretch -->
<div id='align-item-stretch'>
  <style>
  #align-item-stretch {
    margin: 0.3rem;
  }
  #align-item-stretch .outer {
    display: flex;
    width: 100%;
    height: 150px;
    border: 1px solid black;
    align-items: stretch;
    flex-wrap: wrap;
  }
  #align-item-stretch .inner {
    min-width: 30px;
    height: 30px;
    margin: 0.3rem;
    border: 1px solid black;
    background-color:#ccc;
  }
  </style>
  stretch
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
  </div>
</div>

## align-content

<!-- flex-start -->
<div id='align-content'>
<style>
#align-content .outer {
  display: flex;
  width: 80%;
  height: 350px;
  border: 1px solid black;
  flex-wrap: wrap;
}
#align-content .inner {
  height: 30px;
  border: 1px solid black;
  margin: 0.3rem;
  background-color:#ccc;
}
#align-content .item1 {
  width: 20px !important;
}
#align-content .item2 {
  width: 90px !important;
}
#align-content .item3 {
  width: 40px !important;
}
#align-content .item4 {
  width: 70px !important;
}
#align-content .item5 {
  width: 30px !important;
}
#align-content .item6 {
  width: 40px !important;
}
#align-content .item7 {
  width: 70px !important;
}
#align-content .item8 {
  width: 50px !important;
}
#align-content .item9 {
  width: 20px !important;
}
#align-content .item10 {
  width: 200px !important;
}
#align-content .item11 {
  width: 100px !important;
}
#align-content .item12 {
  width: 150px !important;
}
</style>
<div id='align-content-flex-start'>
  <style>
  #align-content-flex-start {
    margin: 0.3rem;
  }
  #align-content-flex-start .outer {
    align-content: flex-start
  }
  </style>
  flex-start
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
    <div class="inner item5">5</div>
    <div class="inner item6">6</div>
    <div class="inner item7">7</div>
    <div class="inner item8">8</div>
    <div class="inner item9">9</div>
    <div class="inner item10">10</div>
    <div class="inner item11">11</div>
    <div class="inner item12">12</div>
  </div>
</div>

<!-- flex-end -->
<div id='align-content-flex-end'>
  <style>
  #align-content-flex-end {
    margin: 0.3rem;
  }
  #align-content-flex-end .outer {
    align-content: flex-end
  }
  </style>
  flex-end
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
    <div class="inner item5">5</div>
    <div class="inner item6">6</div>
    <div class="inner item7">7</div>
    <div class="inner item8">8</div>
    <div class="inner item9">9</div>
    <div class="inner item10">10</div>
    <div class="inner item11">11</div>
    <div class="inner item12">12</div>
  </div>
</div>

<!-- center -->
<div id='align-content-center'>
  <style>
  #align-content-center {
    margin: 0.3rem;
  }
  #align-content-center .outer {
    align-content: center;
  }
  </style>
  center
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
    <div class="inner item5">5</div>
    <div class="inner item6">6</div>
    <div class="inner item7">7</div>
    <div class="inner item8">8</div>
    <div class="inner item9">9</div>
    <div class="inner item10">10</div>
    <div class="inner item11">11</div>
    <div class="inner item12">12</div>
  </div>
</div>

<!-- align-item-space-between -->
<div id='align-content-space-between'>
  <style>
  #align-content-space-between {
    margin: 0.3rem;
  }
  #align-content-space-between .outer {
    align-content: space-between;
  }
  </style>
  space-between
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
    <div class="inner item5">5</div>
    <div class="inner item6">6</div>
    <div class="inner item7">7</div>
    <div class="inner item8">8</div>
    <div class="inner item9">9</div>
    <div class="inner item10">10</div>
    <div class="inner item11">11</div>
    <div class="inner item12">12</div>
  </div>
</div>
<!-- align-item-baseline -->
<div id='align-content-space-around'>
  <style>
  #align-content-space-around {
    margin: 0.3rem;
  }
  #align-content-space-around .outer {
    align-content: space-around;
  }
  </style>
  space-around
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
    <div class="inner item5">5</div>
    <div class="inner item6">6</div>
    <div class="inner item7">7</div>
    <div class="inner item8">8</div>
    <div class="inner item9">9</div>
    <div class="inner item10">10</div>
    <div class="inner item11">11</div>
    <div class="inner item12">12</div>
  </div>
</div>
<!-- align-item-stretch -->
<div id='align-content-stretch'>
  <style>
  #align-content-stretch {
    margin: 0.3rem;
  }
  #align-content-stretch .outer {
    align-content: stretch;
  }
  </style>
  stretch
  <div class="outer">
    <div class="inner item1">1</div>
    <div class="inner item2">2</div>
    <div class="inner item3">3</div>
    <div class="inner item4">4</div>
    <div class="inner item5">5</div>
    <div class="inner item6">6</div>
    <div class="inner item7">7</div>
    <div class="inner item8">8</div>
    <div class="inner item9">9</div>
    <div class="inner item10">10</div>
    <div class="inner item11">11</div>
    <div class="inner item12">12</div>
  </div>
</div>
</div>