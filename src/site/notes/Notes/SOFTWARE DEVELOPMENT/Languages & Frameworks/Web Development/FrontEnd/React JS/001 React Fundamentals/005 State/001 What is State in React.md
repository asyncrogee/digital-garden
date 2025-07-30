---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/005-state/001-what-is-state-in-react/","tags":["programming","ReactJS","javascript","state"],"created":"2025-07-13T15:25:33.898+08:00"}
---


> [!tip] Important information:
> __State__ is the most important concept in React
> 
> _REACT_ is called "React" because:
> IT ___REACTS___ TO __STATE__ CHANGES BY RE-RENDERING THE UI  

![[Pasted image 20250130160728.png]]

---
> [!abstract] State
> - Data that a component __can hold over time__,
> 	- necessary for information that i needs to  ___remember___ throughout the app's lifecycle
> - "__Component's memory__"
> - "__State variable__" / "__piece of state__": A single variable in a component (component state)
> - Updating __component state__ triggers React to ___re-render the component___
> ![[Pasted image 20250130170451.png]]
> - State is how _React_ keeps __UI in-sync with Data__
> ![[Pasted image 20250130170830.png]]

> [!info] State allows developers to:
> 1. Update the component's view (by re-rendering it)
> 2. Persis local variables between renders
> 
> > State is a tool. Mastering state will unlock the power of React  development

### State Example:

```jsx
import { useState } from "react";

const messages = [
  "Learn React ⚛️",
  "Apply for jobs 💼",
  "Invest your new income 🤑",
];

export default function App() {
  const [step, setStep] = useState(1);

  function handlePrevious() { 
	// we have this condition to not go out of bounds:
    if (step > 1) setStep(step - 1);
  }

  function handleNext() {
    if (step < 3) setStep(step + 1);
  }

  return (
    <div className="steps">
      <div className="numbers">
        <div className={`${step >= 1 ? "active" : ""}`}>1</div>
        <div className={`${step >= 2 ? "active" : ""}`}>2</div>
        <div className={`${step >= 3 ? "active" : ""}`}>3</div>
      </div>

      <p className="message">
        Step {step}: {messages[step - 1]}
      </p>

      <div className="buttons">
        <button
          style={{ backgroundColor: "#7950f2", color: "#fff" }}
          onClick={handlePrevious}
        >
          Previous
        </button>
        <button
          style={{ backgroundColor: "#7950f2", color: "#fff" }}
          onClick={handleNext}
        >
          Next
        </button>
      </div>
    </div>
  );
}

```
- `useState` is one of what's called __React Hooks__ (because it has `use` at the beginning)
  
  
> we can only call __Hooks__ like `useState` on the top level of a function:

For example, this is not allowed:
```jsx
if (true) {
  const [step, setStep] = useState(1);
}

// OR inside a function
function sampleFunction() {
  const [step, setStep] = useState(1);
}
```

---

### Bad Practices:

> [!danger] Manual
> ```jsx
> export default function App() {
> 	const [step, setStep] = useState(1);
> 	
> 	function sampleFunction() {
> 		step = step + 1; // Mistake
> 	}
> }
> ```
> - Nothing will happen

> [!caution] Using `object` or `array` for __state__:
> ```jsx
> export default function App() {
> 	const [test] = useState({ name: "Jonas" }); // this object as the initial state
> 	
> 	function sampleFunction() {
> 		test.name = "Fred"; // mutating the object state
> 	}
> }
> ```
> - ___BAD PRACTICE___
