---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/css/layouts/flexbox/","tags":["programming","webdevelopment","frontend","css"],"created":"2024-11-09T11:30:41.417+08:00"}
---


# Flexbox

---

**One-dimensional** CSS layout that can control the way items are spaced out and aligned within a container.

```css
display: flex;
```

This will make an element a **Flex Container**

- Any direct children of a flex container are called **Flex Items**.
  ![Pasted image 20231031100706.png](/img/user/PROGRAMMING/Web%20Development/FrontEnd/CSS/Layouts/attachments/Pasted%20image%2020231031100706.png)
  > [!abstract] Flex Container
  > **_gap: 0_** | `<length>`
  >
  > - To create **space between items,** without using margin
  >
  > **_justify-content: flex-start_** | `flex-end` | `center` | `space-between` | `space-around` | `space-evenly`
  >
  > - To align items along main axis (**horizontally,** by default)
  >
  > **_align-items: stretch_** | `flex-start` | `flex-end` | `center` | `baseline`
  >
  > - To align items along cross axis(**vertically**, by default)
  >
  > **_flex-direction: row_** | `row-reverse` | `column` | `column-reverse`
  >
  > - To define which is the **main axis**
  >
  > **_flex-wrap: nowrap_** | `wrap` | `wrap-reverse`
  >
  > - To allow items to **wrap into new line** if they are too large
  >
  > **_align-content: stretch_** | `flex-start` | `flex-end` | `center` | `space-between` | `space-around`
  >
  > - Only applies when there are **multiple lines** (flex-wrap: wrap)

> [!abstract] Flex Items
> **_align-self: auto_** | `stretch` | `flex-start` | `flex-end` | `center` | `baseline`
>
> - To **overwrite** align-items for individual flex items
>
> **_flex-grow: 0_** | `< integer >`
>
> - To allow an element **to grow** (0 means no, 1+ means yes)
>   - Expand the size of the element to occupy the available spaces
>
> **_flex-shrink: 1_** | `< integer > `
>
> - To allow element **to shrink** (0 means no, 1+ means yes)
>
> **_flex-basis: auto_** | `< length >`
>
> - To define an item's width, **instead of the width** property
>
> **_flex: 0 1 auto_** | `<int> <int> <len>`
>
> - **Recommended** shorthand for flex-grow, -shrink, -basis
>
> **_order: 0_** | `<integer>`
>
> - Controls order of items, -1 makes item **first**, 1 makes it **last**

> [!Example] Flex Property (`flex`,`flex-grow`, `flex-shrink`, `flex-basis`)
>
> ```css
> flex: `<flex-grow>`, `<flex-shrink>`, `<flex-basis>`
> flex: 0 0 200px;
> ```
>
> Flex Basis:
> resize the width of Flex Items but still within the parent container
>
> ```css
> flex-basis: 100px;
>
> /* Default*/
> flex-basis: auto;
> ```
>
> Flex Shrink:
>
> ```css
> flex-shrink: 0;
>
> /*Default:*/
> flex-shrink: 1;
> ```

> [!tip] Flexbox has a main and cross axis.
> `flex-direction` property
>
> - `row` (default): _horizontal axis_ with flex items **from left to right**.
> - `row-reverse`: _horizontal axis_ with flex items **from right to left.**
> - `column`: **_vertical axis_** with flex items from **top to bottom**.
> - `column-reverse`: **_vertical axis_** with flex items from **bottom to top**

> [!tip] `flex-wrap`
> Determines how **_flex items_** behave when the **_flex container_** is **too small**.
>
> - `flex-wrap: wrap;` Allow the items to wrap to the **next row** or **column**.
> - `flex-wrap: nowrap;` (default) will prevent items from wrapping and shrink if needed.

> [!tip] `justify-content`
> Determines how the items inside a **_flex container_** are **positioned** along the main axis, affecting their _position and the space around them_.
>
> - `justify-content: center;`

> [!tip] `align-items`
> Positions the **_flex content_** along the cross axis.
> If `flex-direction: row;`(set to row), the cross axis would be **vertical**
