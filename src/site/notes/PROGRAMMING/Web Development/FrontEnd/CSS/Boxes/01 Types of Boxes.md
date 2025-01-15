---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/css/boxes/01-types-of-boxes/","tags":["programming","webdevelopment","frontend","css"],"created":"2024-11-09T11:30:41.264+08:00"}
---


# 01 Types of Boxes

---

> [!info] Block-level Elements/Boxes
>
> - Blocks of contents which **occupies 100% of parent's element width**
> - Stacked vertically by default
>   > [!example] Default elements
>   > body, main, header, footer, section, nav, aside, div, h1-h6, p, ul, ol, li, etc.
>   >
>   > **with CSS:** display: block

> [!info] Inline Elements/Boxes
>
> - Occupies only space **necessary for its content**
> - Causes **no line-breaks** after or before the element
> - **_Heights and Widths_** do not apply
> - **Paddings and Margins** are applied **_only horizontally_** (left and right)
>   > [!example] Default Elements
>   > a, img, strong, em, button, etc.
>   >
>   > **with CSS**: display: inline

> [!abstract] Inline-Block Boxes
>
> - looks like Inline from the **outside**, behaves like block-level on the **inside**
> - Occupies only content's space
> - Causes no line-breaks
> - Box-model applies
>   > [!example]
>   > **with CSS:** display: inline-block
