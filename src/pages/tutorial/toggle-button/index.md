---
title: Toggle Button
date: 2022-02-01 16:29:03
slug: toggle-button
layout: '../../../layouts/PostLayout.astro'
draft: true
---

Considerations for an accessible toggle button:

Honestly, there aren't all that many considerations if you use a real `<button>` element. In order to indicate that the button is pressed properly, though, you'll want to forego adding or removing classes in favor of setting `aria-pressed="true"`.

Selecting `button[aria-pressed="true"]` is just as easy as selecting a button with any given class, (and has greater specificity than just selecting a class by itself,) and you gain all the benefits of indicating the button's state to any technology that relies on it.

Resources:
[Adrian Roselli - Under-Engineered Toggles Too](https://adrianroselli.com/2019/08/under-engineered-toggles-too.html)

```js
console.log('Hello, world.);

const button = 'Okay then';
```