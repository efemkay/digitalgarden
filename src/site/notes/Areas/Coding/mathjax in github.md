---
{"dg-publish":true,"dg-path":"Coding/mathjax in github.md","permalink":"/coding/mathjax-in-github/","tags":["Reference"],"created":"2022-07-15","updated":"2024-07-21"}
---


- #### Since May 2022 Github repo (only the repo, not yet for GH Pages) supports math expression in TeX / [[Areas/General/LATEX\|LATEX]] so you can use it for GH Readme
	- it follows mathjax syntax that can be used together in markdown document, e.g.
		```markdown
		When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
		$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $
		```
	- will render as
		- ![](https://github.blog/wp-content/uploads/2022/05/Math-markdown-post.png)
	- To add mathjax support for GH Pages see [[Areas/Coding/add mathjax to github pages and jekyll\|add mathjax to github pages and jekyll]]
- #### There’s an alternative to loading mathjax using a custom javascript for showing mathematical equations.
	- This is pulled from TeXt theme github repo **but I haven’t test it**
		```html
		{% raw %}
		<script type="text/x-mathjax-config">
			var _config = { tex2jax: {
				inlineMath: [ ['
		- [r] [jekyll-TeXt-theme/mathjax.html at master · kitian616/jekyll-TeXt-theme (github.com)](https://github.com/kitian616/jekyll-TeXt-theme/blob/master/_includes/markdown-enhancements/mathjax.html)

## References
- [Math support in Markdown | The GitHub Blog](https://github.blog/2022-05-19-math-support-in-markdown/)
- [Writing mathematical expressions - GitHub Docs](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
,'
		- [r] [jekyll-TeXt-theme/mathjax.html at master · kitian616/jekyll-TeXt-theme (github.com)](https://github.com/kitian616/jekyll-TeXt-theme/blob/master/_includes/markdown-enhancements/mathjax.html)

## References
- [Math support in Markdown | The GitHub Blog](https://github.blog/2022-05-19-math-support-in-markdown/)
- [Writing mathematical expressions - GitHub Docs](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
], ['\\(','\\)'] ]
			}};
			
			{%- if _mathjax_autoNumber == true -%}
				_config.TeX = { equationNumbers: { autoNumber: "all" } };
			{%- endif -%}
			
			MathJax.Hub.Config(_config);
		</script>
		<script type="text/javascript" src="{{ _sources.mathjax }}" async></script>
		{% endraw %}
		```
		- [r] [jekyll-TeXt-theme/mathjax.html at master · kitian616/jekyll-TeXt-theme (github.com)](https://github.com/kitian616/jekyll-TeXt-theme/blob/master/_includes/markdown-enhancements/mathjax.html)

## References
- [Math support in Markdown | The GitHub Blog](https://github.blog/2022-05-19-math-support-in-markdown/)
- [Writing mathematical expressions - GitHub Docs](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
