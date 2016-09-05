#Extra Syntax

###Footnotes
Footnotes work mostly like reference-style links. A footnote is made of two things: a marker in the text that will become a superscript number; a footnote definition that will be placed in a list of footnotes at the end of the document. A footnote looks like this:

	That's some text with a footnote.[^1]

	[^1]: And that's the footnote.
	
###Strikethrough
Wrap with 2 tilde ~ characters:

	~~Strikethrough~~
	
###Fenced Code Blocks
Start with a line containing 3 or more backtick ` characters, and ends with the first line with the same number of backtick `:

	```
	Fenced code blocks are like Stardard
	Markdown’s regular code blocks, except that
	they’re not indented and instead rely on a
	start and end fence lines to delimit the code
	block.
	```
	
###Tables
A simple table looks like this:

	First Header | Second Header | Third Header
	------------ | ------------- | ------------
	Content Cell | Content Cell  | Content Cell
	Content Cell | Content Cell  | Content Cell
	
If you wish, you can add a leading and tailing pipe to each line of the table:

	| First Header | Second Header | Third Header |
	| ------------ | ------------- | ------------ |
	| Content Cell | Content Cell  | Content Cell |
	| Content Cell | Content Cell  | Content Cell |
	
Specify alignement for each column by adding colons to separator lines:

	First Header | Second Header | Third Header
	:----------- | :-----------: | -----------:
	Left         | Center        | Right
	Left         | Center        | Right
	
###Anchor
You can also add an anchor for an element such as Headers, then you can link to this anchor anywhere, when you click that link in the Preview view, it'll auto scroll to the place of the destination anchor.   
For example below is a normal h2 Header:

	## This is an example
	
Now we add an anchor for it, here we use the name "anchor1" for the anchor, of course you can use any name you want

	## [This is an example](id:anchor1)
	
If you want to link to this anchor, simply write like this:

	Click this [link](#anchor1) in the Preview view will auto scroll to the place of the destination anchor.

