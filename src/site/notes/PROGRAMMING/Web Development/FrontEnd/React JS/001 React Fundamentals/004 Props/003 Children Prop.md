---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/004-props/003-children-prop/","tags":["programming","ReactJS","javascript","props"],"created":"2025-02-09T15:58:52.635+08:00"}
---

> [!abstract] Children Prop
> ![Pasted image 20250209162244.png](/img/user/Misc/attachments/Pasted%20image%2020250209162244.png)
> - The `children prop` allow us to __pass JSX into an element__ (besides regular props)
> - Essential tool to make __reusable__ and __configurable__ `components` (especially `component`_content_)
> - Really useful for __generic__ `components` that __don't know their content__ before being used (e.g. modal)


#### Example:
We created a __re-usable `Button Component`__ and pass the contents as `props`
```jsx
  <div className="buttons">
	<Button 
	  bgColor='#7950f2' textColor="#fff" 
	  onClick={handlePrevious}
	  text="Previous"
	  emoji="👈"
	/>
	<Button 
	  bgColor='#7950f2' textColor="#fff" 
	  onClick={handleNext}
	  text="Next"
	  emoji="👉"
	/>
  </div>
// ...

function Button({ textColor, bgColor, onClick, text, emoji }) {
  return (
    <button
      style={{ backgroundColor: bgColor, color: textColor }}
      onClick={onClick}
    >
      <span>{emoji}</span> {text}
    </button>
  );
}
```
- the problem here, is that we want the emoji in the "`Next button`" to be on the right side.
	- ![[Pasted image 20250209160341.png \| 300]]

### Children Prop
What we can do is to make the `Emoji` and `Text` as __Children Props__
```jsx
  <div className="buttons">
	<Button 
	  bgColor='#7950f2' textColor="#fff" 
	  onClick={handlePrevious}>
		<span>👈</span> Previous
	</Button>
	<Button 
	  bgColor='#7950f2' textColor="#fff" 
	  onClick={handleNext}>
		Next <span>👉</span>
	</Button>
  </div>
```
- The `Component element` is not automatically closed (`<Button>...</Button>`)
- and we __put the `children prop` content inside of those `<Tags>`__ 

```jsx
function Button({ textColor, bgColor, onClick, children }) {
  return (
    <button
      style={{ backgroundColor: bgColor, color: textColor }}
      onClick={onClick}
    >
      {children}
    </button>
  );
}
```
- and then, we call the `children prop` as __children__ (it's already __pre-defined__ in _ReactJS_)

### More Examples:
```jsx
function StepMessage({ step, children }) {
  return (
    <div className="message">
      <h3>Step {step}</h3>
      {children}
    </div>
  );
}

export default function Project3() {
  return (
    <div>
      <Steps />
      <StepMessage step={1}>
        <p>Pass in content</p>
        <p>*</p>
      </StepMessage>
    </div>
  );
}
```

###### Component inside an `HTML element` INSIDE a Component
```jsx
  <StepMessage step={step}>
	{messages[step - 1]}
	<div className="buttons">
	  <Button bgColor="#e7e7e7" textColor="#333" 
		onClick={() => alert(`Learn how to ${messages[step - 1]}`)}>
		  Learn how
	  </Button>
	</div>
  </StepMessage>

  <StepMessage step={step}>
	{messages[step - 1]}
  </StepMessage>
```