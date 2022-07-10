---
{"dg-publish":true,"permalink":"/areas/public/stack-edit-custom-css-for-blogger/","dgHomeLink":true,"dgPassFrontmatter":false}
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
- topic:: [[Areas/Public/MOCs/00 Coding|00 Coding]]
	- related:: [[Areas/General/css snippets|css snippets]]
- updated:: [[journals/2022/07/2022-07-02|2022-07-02]]
- reviewed:: [[journals/2022/07/2022-07-02|2022-07-02]]
- #FleetingNote 