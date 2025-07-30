---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/003-jsx/002-imperative-vs-declarative/","tags":["programming","ReactJS","javascript","jsx"],"created":"2025-07-13T15:24:50.943+08:00"}
---


> [!info] Imperative
> We tell the browser exactly "__How to do things__"
> ![[Pasted image 20241228162322.png]]
> - Manual DOM element selections and DOM traversing
> - Step-by-step DOM mutations until we reach the desired UI

> [!tip] Declarative
> Using _JSX_ we tell _React_ "__What we want__" to see in the screen, but not step-by-step.
> ![[Pasted image 20241228162429.png]]
> - Describe what UI should look like using _JSX_, __based on current data__
> - React is an __abstraction__ away from DOM: ___we never touch the DOM___
> - Instead, we think of the UI as a __reflection of the current data__

