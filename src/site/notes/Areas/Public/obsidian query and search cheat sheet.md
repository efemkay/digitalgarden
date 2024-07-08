---
{"dg-publish":true,"dg-path":"Public/obsidian query and search cheat sheet.md","permalink":"/public/obsidian-query-and-search-cheat-sheet/","title":"obsidian query and search cheat sheet","tags":["Reference"],"created":"2022-12-01","updated":"2024-07-08"}
---


- #### (The vanilla) Obsidian query only supports search parameters i.e. searching for either in file name, tags, blocks, etc. but nothing on how the results are rendered or displayed
	- you can specify where the text is expected to be found i.e. in the file name or note’s content and as such these parameters are available
		- `file:`
		- `path:`
		- `tag:`
		- `line:`
		- `section:`
		- `block`
	- you may also narrow the find to just markdown tasks with the following parameters
		- `task:`
		- `task-todo:`
		- `task-done:`
	- ![FgKJBDeWIAAwKDU (595×842) (twimg.com)](https://pbs.twimg.com/media/FgKJBDeWIAAwKDU?format=png&name=900x900)
- #### Typical Obsidian query looks like code block below where you can combine several parameters to help narrow down the results
	- In the example below, it is looking for any notes where
		- (a) any of its blocks contain word “productivity”, but
		- (b) only for notes with tags `#permanentnote`, and
		- (c) exclude results from file that path contains the word “journal”
		````
		```query
		block: "productivity"
		tag: (permanentnote)
		-path: journals
		```
		````
- #### You may “beautify” and makes the output more functional with additional plugin. See my additional notes as per links below
	- [[Areas/Public/Improved Obsidian query with NIL Query Control and custom css\|Improved Obsidian query with NIL Query Control and custom css]]
	- [[Areas/Public/Obsidian Query Control plugin refine how the output looks like\|Obsidian Query Control plugin refine how the output looks like]]


## References
- https://mobile.twitter.com/heymichellemac/status/1585980871248867328