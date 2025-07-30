---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/react-js/001-react-fundamentals/003-jsx/007-react-fragment/","tags":["programming","ReactJS","javascript","reactfragment","jsx"],"created":"2025-07-13T15:25:33.852+08:00"}
---

> [!abstract] React Fragment
> Let's us __group some elements__ without leaving any trace in the `HTML tree` / `DOM`
> 
> Sometimes we need 2 elements but _JSX_ ___only allows 1 root element___
> - We often solve this by wrapping them inside a `<div>`
> 	- but, we may not want to render a single element because it might mess up the layout of the design.
> 
> - Syntax: `<> </>`

 ```js
       {numPizzas > 0 ? (
        <>
          <p>
            Authentic Italian cuisine. & creative dishes to choose from. All
            from our stone oven, all organic, all delicious.
          </p>
          <ul className="pizzas">
            {pizzas.map((pizza) => (
              <Pizza pizzaObj={pizza} key={pizza.name} />
            ))}
          </ul>
        </>
      ) : (
        <p>We're still working on our menu. Please come back later :)</p>
      )}
```
- `<> </>` This is the __React Fragment__
- We wrapped `<p>` and `<ul>`
- It didn't create any parent element in the `DOM Tree` (nothing shows in the browser console inspect)

---
Sometimes we need a `key` in a __React Fragment__
- example is when we're using it to __render a list__

```js
      {numPizzas > 0 ? (
        <React.Fragment key='example'>
          <p>
            Authentic Italian cuisine. & creative dishes to choose from. All
            from our stone oven, all organic, all delicious.
          </p>
          <ul className="pizzas">
            {pizzas.map((pizza) => (
              <Pizza pizzaObj={pizza} key={pizza.name} />
            ))}
          </ul>
        </React.Fragment>
      ) : (
        <p>We're still working on our menu. Please come back later :)</p>
      )}
```
