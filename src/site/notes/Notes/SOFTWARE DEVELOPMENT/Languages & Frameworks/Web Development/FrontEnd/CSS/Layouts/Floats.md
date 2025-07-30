---
{"dg-publish":true,"permalink":"/notes/software-development/languages-and-frameworks/web-development/front-end/css/layouts/floats/","tags":["programming","webdevelopment","frontend","css"],"created":"2025-07-13T15:24:55.493+08:00"}
---


# Floats

---

- Element is removed from the normal flow: "out of flow"
- Text and inline elements will wrap around the floated element
- The container will **not** adjust its height to the element
  > [!abstract] Float
  > The image will be out of the page's flow (like _position: absolute_)
  >
  > ```css
  > .author-img {
  >   float: left;
  > }
  > ```
  >
  > ![[Pasted image 20231031034324.png]]
  > The text float besides the image

> [!caution] Collapsing Elements
> The container that contains
