---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/005-state/002-mechanism-of-state/","tags":["programming","ReactJS","javascript","state"],"created":"2025-07-13T15:25:33.893+08:00"}
---


# Mechanics of State in ReactJS

> [!info] Mechanics of State
> - ReactJS is _declarative_, meaning we don't do `DOM manipulations`
> - __a view is updated by re-rendering the component__
> 	- _ReactJS_ calls the `component function` again, but the __State is preserved__ throughout re-renders
> 
> ![[Pasted image 20250130214155.png]]

> [!example] Examples
> ![[Pasted image 20250130214436.png]]
> - When we click "`Get Advice`" button, a new advice is stored in `advice` from an API
> - The `count` and `advice` is then updated by the `setAdvice` and `setCount` functions
> 
> ![[Pasted image 20250130214608.png]]


