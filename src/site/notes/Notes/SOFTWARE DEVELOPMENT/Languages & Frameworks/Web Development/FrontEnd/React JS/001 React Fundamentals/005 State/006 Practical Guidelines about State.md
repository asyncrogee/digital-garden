---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/005-state/006-practical-guidelines-about-state/","tags":["programming","ReactJS","javascript","state"],"created":"2025-07-13T15:25:33.884+08:00"}
---

## Practical Guidelines about State

> [!tip] Remember
> Use a __state variable__ for any data that the `component` should __keep track of__ ("__remember__") over time.
> 
> ___This is data that will change at some point___.
> 
> In Vanilla JS, that's a `let` variable, or an `[]` or `{}`

> [!tip] Dynamic
> Whenever you want something in the component to be __dynamic__, create a piece of `state` related to that "thing", 
> 
> and update the state when the "thing" should change (aka "be dynamic")
> 
>> [!example]
>> A modal window can be open or closed.
>> 
>> So we create a state variable `isOpen` that tracks whether the modal is open or not.
>> 
>> On is `isOpen = true` we display the window, on `isOpen = false` we hide it.

> [!tip] Looks
> If you want to change the way a component looks, or the data it displays, __update its state__.
> 
> This usually happens in an __event handler__ function.

> [!tip] Reflection
> When building a component, imagine its view as a __reflection of state changing over time__

> [!tip] Mistake: Data that will not re-render
> For data that should not trigger ___component re-renders___, __don't use state__.
> 
> Use a `regular variable` instead.
> 
> This is a common ___beginner mistake___



