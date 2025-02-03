---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/005-state/003-updating-state-based-on-current-state/","tags":["programming","ReactJS","javascript","state"],"created":"2025-01-30T22:16:24.743+08:00"}
---


```jsx
export default function App() {
  const [step, setStep] = useState(1);
  const [isOpen, setIsOpen] = useState(true);

  function handlePrevious() {
    if (step > 1) setStep(step - 1);
  }

  function handleNext() {
    if (step < 3) {
      setStep(step + 1);
    }
  }

  return (
    <>
      <button className="close" onClick={() => setIsOpen(!isOpen)}>
        &times;
      </button>
// ...
```

- This works just fine, but in some case where we need to modify the code like using the `setState` multiple times:

> [!danger] That would not work
>```jsx
  >function handleNext() {
>    if (step < 3) {
> 	setStep(step + 1);
>	setStep(step + 1);
>	}
 > }
>```

> [!done] Use an arrow function:
> ```jsx
> function handlePrevious() {
> 	if (step > 1) setStep((s) => s - 1);
> }
> 
> function handleNext() {
> 	if (step < 3) {
> 		setStep((s) => s + 1);
> 		setStep((s) => s + 1);
> 		setStep((s) => s + 1); // This would now work!
> 	}
> }
> 
> return (
> 	<>
> 		// Also here in the open & close button:
> 		<button> className="close" onClick={() => setIsOpen((is) => !is)}> 
>  )
>  ```

