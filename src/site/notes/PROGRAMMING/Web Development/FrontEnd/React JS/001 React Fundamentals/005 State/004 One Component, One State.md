---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/005-state/004-one-component-one-state/","tags":["programming","ReactJS","javascript","state"],"created":"2025-01-31T22:47:07.131+08:00"}
---


 Each component has and manages __its own state__, no matter how many times we render the same component
 
 - Each _instances_ of a `component` (when a `component` is used __multiple times__) will operate independently

 ![[Pasted image 20250201161416.png \| 400]]
 - Changes from an _instance_ will not affect the other `components`:
 ![[Pasted image 20250201161517.png \| 400]]
- like when clicking the other button,
- deleting an _instance_

#### Example:

```jsx
import { useState } from "react";

const messages = [
  "Learn React ⚛️",
  "Apply for jobs 💼",
  "Invest your new income 🤑",
];

export default function App() {
  return (
    <>
      <Steps />
      <Steps />
    </>
  );
}

function Steps() {
  const [step, setStep] = useState(1);
  const [isOpen, setIsOpen] = useState(true);

  function handlePrevious() {
    if (step > 1) setStep((s) => s - 1);
  }

  function handleNext() {
    if (step < 3) {
      setStep((s) => s + 1);
    }
  }

  return (
    <>
      <button className="close" onClick={() => setIsOpen((is) => !is)}>
        &times;
      </button>

      {isOpen && (
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
      )}
    </>
  );
}

```
- We declared `<Steps />` component twice