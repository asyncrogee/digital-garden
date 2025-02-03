---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/001-intro-and-theories/006-state-vs-props/","tags":["programming","ReactJS","javascript","props","state"],"created":"2025-02-03T13:44:30.577+08:00"}
---


| State                                                                                                                                                 | Props                                                                                                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| - __Internal data__, owned by `component`<br>![[Pasted image 20250203134557.png \| 300]]                                                              | - ___External data___, owned by `parent component`<br>![[Pasted image 20250203134742.png]]                                                     |
| `Component's` "MEMORY"                                                                                                                                | - Similar to ___function `parameters`___<br>                                                                                                   |
| - Can be updated by the `component` itself<br>- _Updating_ `state` causes `component` to __re-render__<br>![[Pasted image 20250203135056.png \| 300]] | - Read-only<br>- ___Receiving new `props`___ causes `component` to __re-render__<br>- Usually when the parent's `state` has been ___updated___ |
| - Used to make `components` __interactive__                                                                                                           | - Used by ___parent___ to configure __child component__ ("settings")                                                                           |
