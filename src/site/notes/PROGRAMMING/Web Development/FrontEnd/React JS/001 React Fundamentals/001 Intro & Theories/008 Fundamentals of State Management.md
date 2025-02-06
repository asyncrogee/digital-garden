---
{"dg-publish":true,"permalink":"/programming/web-development/front-end/react-js/001-react-fundamentals/001-intro-and-theories/008-fundamentals-of-state-management/","tags":["programming","ReactJS","javascript","state"],"created":"2025-02-04T21:38:13.022+08:00"}
---

> [!abstract] State Management:
> - Deciding __when__ to create pieces of `state`, 
> - what __types__ are necessary, 
> - __where__ to place each piece of `state`,
> - how data __flows__ through the app

| __Local State__                                                                                                                      | ___Global State___                                                                   |
| ------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| - `State` needed __only by one or few components__                                                                                   | `State` that __many components__ might need                                          |
| `State` that is defined in a component and __only that `component` and child components__ have access to it (by passing via `props`) | __Shared__ state that is accessible to __every component__ in the entire application |
| __We should always start with local state__                                                                                          | Using _Context API_ or _Redux_                                                       |

### STATE: When and Where?
![Pasted image 20250206215723.png](/img/user/Misc/attachments/Pasted%20image%2020250206215723.png)