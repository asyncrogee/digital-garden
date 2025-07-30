---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/003-jsx/005-conditional-rendering-with-and-and/","tags":["programming","ReactJS","javascript","jsx"],"created":"2025-07-13T15:25:33.858+08:00"}
---

---
```js
function Footer() {
  const hour = new Date().getHours();
  const openHour = 0;
  const closeHour = 23;
  const isOpen = hour >= openHour && hour <= closeHour;
  console.log(isOpen);

  return (
    <footer className="footer">
    
// Here we did a short-circuiting using the && operator
      {isOpen && (
        <div className="order">
          <p>We're open until {closeHour}:00. Come visit us or order online.</p>
          <button className="btn">Order</button>
        </div>
      )}
    </footer>
  );

}
```


> [!danger]- Wrong Example:
> ```js
> function Menu() {
> 	// For example, pizza is empty
> 	const pizzas = [];
> 	const numPizzas = pizzas.length;
> 	
> 	return (
> 		<main className="menu">
> 				<h2>Our Menu</h2>
> 				
> 				{numPizzas  && (
> 					<ul className="pizzas">
> 						{pizzas.map((pizza) => (
> 							<Pizza pizzaObj={pizza} key={pizza.name} />
> 						))}
> 					</ul>	
> 				)}
> 		);
> }
> ```
> - because we're using `numPizzas` straight up which is an integer `0`, the page will display the number `0`.
> 	- Instead of it not actually rendering anything.


Here we compare if `numPizzas > 0` which would return a boolean value:
```js
 function Menu() {
	 const pizzas = pizzaData;
	 const numPizzas = pizzas.length;
	 
	 return (
		 <main className="menu">
			 <h2>Our Menu</h2>
			 
			 {numPizzas > 0 && (
				 <ul className="pizzas">
					 {pizzas.map((pizza) => (
						 <Pizza pizzaObj={pizza} key={pizza.name} />
					 ))}
				</ul>
			 )}
		</main>
	 );
 }
```

