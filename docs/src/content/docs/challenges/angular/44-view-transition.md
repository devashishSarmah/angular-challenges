---
title: 🔴 View Transition
description: Challenge 44 is about learning the new view transition animation API
author: thomas-laforge
challengeNumber: 44
command: angular-view-transition
sidebar:
  order: 208
  badge: New
---

## Information

The View Transition API is a brand new API that provides a set of features that allow developers to control and manipulate the transitions and animations between views within an application.
It plays a pivotal role in enhancing user experience (UX), bringing applications to life with engaging and captivating transitions to guide users through different pages or sections of the app.

The goal of this challenge is to learn about and manipulate all types of transitions proposed by the API.

To use the API, Angular provides a function `withViewTransitions()` that needs to be injected inside the router config.

I would advise you to read the [Chrome documentation](https://developer.chrome.com/docs/web-platform/view-transitions). You will learn everything necessary to successfully complete the challenge.

Here, however, is a short summary:
Firstly, each target DOM element has two states; an `old` one when the element is leaving the page, and a `new` one when it's entering the page:

```css
::view-transition-old(root) {
/ / animation
}

::view-transition-new(root) {
/ / animation
}
```

In order to target a specific element, you must add the selector `view-transition-name` to a CSS class on the DOM node, as shown below:

```css
.specific-element {
  view-transition-name: specific-element;
}
```

This allows you to create an animation for this element only.

Lastly, if the same element is present in both views, you can automate the transition by assigning the same **transition name**.

:::danger
Remenber, you can have only ONE UNIQUE `view-transition-name` per page.
:::

## Statement

The goal of this challenge is to transition from the state shown in this video:

To the final state shown in the following video:

Observe the following:

- The header slides in and out
- Each element smoothly transitions to its new location

### Level 1

Focus only on the first thumbnail and create a seamless and pleasing transition

### Level 2

Create the same appealing transition for all thumbnails without duplicating the `view-transition-name`. Note that this page has only 3 thumbnails; in a real-life scenario, you could have significantly more.

### Level 3

Shift to the correct Y location when navigating back and forth.