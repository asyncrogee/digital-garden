---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/001-intro-and-theories/007-thinking-in-react/","tags":["programming","ReactJS","javascript","JS-Fundamentals","theory"],"created":"2025-07-13T15:25:33.861+08:00"}
---


> [!tip]
> To build React Apps:
> - know How to work with React API
> - Think in React "React Mindset"
>   ![[Pasted image 20250204211621.png \| 400]]

> [!info] Thinking in React
> - "React Mindset"
> - Thinking about `components`, __state__, _data flow_, ___effects___, etc.
> - Thinking in __state transitions__, not element mutations
>   
>> [!abstract] The "Thinking in React" Process (not a rigid process)
>> 1. Break the desired UI into `components` and establish the __component tree__
>>    - also thinking about _re-usability_ and ___composability___ of `components`
>> 2. Build __static__ version in React (without state)
>>    
>>    __STATE MANAGEMENT__:
>> 3. Think about __STATE__:
>>    - When to use `state`
>>    - Types of state: _local_ vs __global__
>>    - Where to place each piece of `state`
>> 4. Establish ___data flow___:
>>    - One-way data flow
>>    - Child-to-parent communication
>>    - Accessing global `state`

![[Pasted image 20250204212520.png]]