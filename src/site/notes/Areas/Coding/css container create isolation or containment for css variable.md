---
{"dg-publish":true,"dg-path":"Coding/css container create isolation or containment for css variable.md","permalink":"/coding/css-container-create-isolation-or-containment-for-css-variable/","tags":["PermanentNote"],"created":"2023-09-07","updated":"2024-01-26"}
---

- #### CSS `@container` will “contain” any variable declaration within in – meaning that if i declare `@container` at `.body > .section`, i cannot affect anything at `.body`
- #### With `@container`, I can use container query length units i.e. `cqw`, `cqh`, `cqi`, `cqb` to get information about the container’s size
	- In the same way that `vh` and `vw` are relative to the size of the viewport, container query units are relative to the size of their container.
		- cqw (Container Query Width) – 1% of the container’s width
		- cqh (Container Query Height) – 1% of the container’s height
		- cqi (Container Query Inline) – 1% of the container’s inline size
		- cqb (Container Query Block) – 1% of the container’s block size
	- ![](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries/container-query.svg)

## References
- [Shiny, new CSS features to get to know - StatusCake](https://www.statuscake.com/blog/new-css-features-to-get-to-know/)
- [Digging Deeper Into Container Style Queries | CSS-Tricks - CSS-Tricks](https://css-tricks.com/digging-deeper-into-container-style-queries/)
- [CSS container queries - CSS: Cascading Style Sheets | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries)
- [A guide to CSS container queries - LogRocket Blog](https://blog.logrocket.com/css-container-queries-guide/)