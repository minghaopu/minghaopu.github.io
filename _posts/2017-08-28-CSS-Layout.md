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

<div>
  <style>
  .outer {
    display: flex;
    width: 100%;
    height: 300px;
    border: 1px solid black;
    align-items:center;
    justify-content:center;
  }
  .inner {
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