---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/css/layouts/box-sizing-border-box/","tags":["programming","webdevelopment","frontend","css"],"created":"2025-07-13T15:24:55.500+08:00"}
---


# box-sizing border-box

---

Opposite of `content-box`

```css
box-sizing: border-box;
```

![[Pasted image 20231031080814.png]]

- Total width of the element, including padding and border, will be the **explicit width set**
- adding padding will make the size of the content adjust.
  - The **content of the element** will shrink to make room for the _padding and border_.
