---
{"dg-publish":true,"permalink":"/areas/public/stack-edit-custom-css-for-blogger/","title":"StackEdit custom css for Blogger","updated":"2023-08-30T22:09:54.972+08:00"}
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

## Metadata
- topic:: [[Areas/Public/MOCs/00 Coding\|00 Coding]]
	- related:: [[Areas/Public/CSS Notes\|CSS Notes]]
- updated:: [[journals/2022/07/2022-07-02\|2022-07-02]]
- reviewed:: [[journals/2022/07/2022-07-02\|2022-07-02]]
- #FleetingNote #toexpand 
	- Add outliner snippet i just did for blogger