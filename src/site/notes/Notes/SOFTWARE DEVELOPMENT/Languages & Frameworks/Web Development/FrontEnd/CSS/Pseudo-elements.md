---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/css/pseudo-elements/","tags":["programming","webdevelopment","frontend","css"],"created":"2025-07-13T15:24:55.525+08:00"}
---


While **Pseudo-classes** uses One(1) Semi-colon `:`

**_Pseudo-elements_** uses Two(2) Semi-colon `::`

```css
h1::first-letter {
  font-style: normal;
  margin-right: 5px;
}

p::first-line {
  color: red;
}
```

> [!example] Adjacent Siblings Pseudo-element
> Only the first line of the **paragraphs** adjacent to **h3** will be modified
>
> ```css
> h3 + p::first-line {
>   color: red;
> }
> ```

> [!tip] After Pseudo-element
> Creates a pseudo-element that will be the **very first child** of the selected element
>
> - No need to create a new element
>
> ```css
> h2:after {
>   content: "TOP";
>   background-color: #ff370e;
>   color: #444;
>   font-size: 16px;
>   font-weight: bold;
>   display: inline-block;
>   padding: 5px 10px;
>   position: absolute;
>   top: -10px;
>   right: -25px;
> }
> ```

```

```
