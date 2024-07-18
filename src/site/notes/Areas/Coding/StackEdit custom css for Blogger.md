---
{"dg-publish":true,"dg-path":"Coding/StackEdit custom css for Blogger.md","permalink":"/coding/stack-edit-custom-css-for-blogger/","title":"StackEdit custom css for Blogger","tags":["FleetingNote"],"updated":"2022-07-02"}
---


- #### StackEdit already has a beautiful css formatting for html export, which can be used to publish to blogger but with few exceptions
	- max-width set to only 750px and inline padding of 30px – this affect if the html is placed within another div (as blogger does for “content”)
- #### To override this, I add the following line into `div` `stackedit__html`
	- `style="max-width: 100%; padding-left: 10px; padding-right: 10px;">`
	- resulting in the following
		```html
		<div class="stackedit__html" style="max-width: 100%; padding-left: 10px; padding-right: 10px;">
			{{{files.0.content.html}}}
		</div>
		```

> [!todo]
> - related:: [[Areas/Public/CSS Notes\|CSS Notes]]
> - [ ] Add outliner snippet i just did for blogger #toexpand 

