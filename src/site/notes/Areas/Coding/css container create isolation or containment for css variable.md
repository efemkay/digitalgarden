---
{"dg-publish":true,"dg-path":"Coding/css container create isolation or containment for css variable.md","permalink":"/coding/css-container-create-isolation-or-containment-for-css-variable/","tags":["PermanentNote"],"created":"2023-09-07","updated":"2024-01-26"}
---

- #### When using a container query, we give elements the ability to change based on their _container’s size_, not the viewport.
	- CSS `@container` will “contain” any variable declaration within in – meaning that if i declare `@container` at `.body > .section`, i cannot affect anything at `.body`
- #### A container cannot change its own styles, Rather, they change the styles of ==their contents instead==
	- *“You cannot style what you query”* is a way to think about it.
	- We cannot change the container’s `background-color` when it is a certain size — but we can change the `background-color` of any element _inside_ the container. 
- #### With @container, I can use container query length units i.e. `cqw`, `cqh`, `cqi`, `cqb` to get information about the container’s size
	- In the same way that `vh` and `vw` are relative to the size of the viewport, container query units are relative to the size of their container.
		- cqw (Container Query Width) – 1% of the container’s width
		- cqh (Container Query Height) – 1% of the container’s height
		- cqi (Container Query Inline) – 1% of the container’s inline size
		- cqb (Container Query Block) – 1% of the container’s block size
	- ![](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_containment/Container_queries/container-query.svg)

---

- [i] Here’s an example used to do Wide Blocks in Obsidian
```css
/* -- Setup for @container -- */
:is(.wide-table, .wide-dataview, .wide-callout, .wide-backlinks).markdown-source-view.is-readable-line-width,
:is(.wide-table, .wide-dataview, .wide-callout, .wide-backlinks).markdown-preview-view.is-readable-line-width {
	container-name: content-view;
	container-type: inline-size;
}

/* === Wide Blocks - Wide Table === */

/* -- Main Code - EV & RV -- */
body {
	--wide-tbl-left-ev-adj: -4rem;
	--wide-tbl-min-left-ev: 0.5rem;
	--wide-tbl-width-ev: calc( var(--file-line-width) - var(--wide-tbl-left-ev-adj) );
}
body:has(.cm-gutters) {
	--wide-tbl-left-ev-adj: 1rem;
	--wide-tbl-min-left-ev: 6rem;
}

@container content-view (width > 50px) {
	/* editing view */
	:is(.wide-table-global, .wide-table) .cm-embed-block.cm-table-widget {
		width: calc(100cqi - 4rem);
		margin-left: calc( max( 100cqi - var(--wide-tbl-width-ev), var(--wide-tbl-min-left-ev) ) / 2 * -1 ) !important;
	}
	
	/* reading view */
	:is(.wide-table-global .markdown-preview-view, .wide-table.markdown-preview-view) div:has(> table) {
		width: 100cqi;
		margin-left: calc( max( 100cqi - var(--file-line-width), 1rem ) / 2 * -1 ) !important;
	}
}
```

## References
- [CSS Container Queries | CSS-Tricks](https://css-tricks.com/css-container-queries/)
- [Shiny, new CSS features to get to know - StatusCake](https://www.statuscake.com/blog/new-css-features-to-get-to-know/)
- [Digging Deeper Into Container Style Queries | CSS-Tricks - CSS-Tricks](https://css-tricks.com/digging-deeper-into-container-style-queries/)
- [CSS container queries - CSS: Cascading Style Sheets | MDN (mozilla.org)](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_container_queries)
- [A guide to CSS container queries - LogRocket Blog](https://blog.logrocket.com/css-container-queries-guide/)