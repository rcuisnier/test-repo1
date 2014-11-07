Heading 1
==========

Heading2
 =======
 
 Sub-heading
 -----------
 
### Another deeper heading

### Paragraphs
A paragraph is simply one or more consecutive lines of text, separated by one or more blank lines.   
A blank line is any line that looks like a blank line (a line containing nothing but spaces or tabs is considered blank.)  
Normal paragraphs should not be indented with spaces or tabs.
 
Paragraphs are separated by a 
blank line.
 
Let 2 spaces at the end of a line to do a  
line break
 
Text attributes *italic*, **bold**, `monospace`,~~monospace~~, `monospace` , _emphasis_ __bold__


## Links
 
 A [link](http://example.com).    
 [example link](http://example.com/ "With a Title").  
 Another link : <http://example.com/>  
 Mailto : <test@test.com>  

### Links reference

Reference-style links allow you to refer to your links by names, which you define elsewhere in your document:

I get 10 times more traffic from [Google][1] than from
[Yahoo][2] or [MSN][3].

[1]: http://google.com/        "Google"
[2]: http://search.yahoo.com/  "Yahoo Search"
[3]: http://search.msn.com/    "MSN Search"

## Images

Image syntax is very much like link syntax.

Inline (titles are optional):

![alt text](/path/to/img.jpg "Title")

### Reference-style:

![alt text][id]

[id]: /path/to/img.jpg "Title"

Both of the above examples produce the same output:


## Others
 <<<   No space between ] and (  >>>
 
### Horizontal rules
* * *

***

*****

- - -

---------------------------------------
 
### Specials characters
 &copy;
 &gt; 
 &lt;
 :)
 &#8212;
 &mdash; - _ -- 
 
 
## Unordered Lists

*   Candy.
*   Gum.
*   Booze.

this:

+   Candy.
+   Gum.
+   Booze.

and this:

-   Candy.
-   Gum.
-   Booze.

 
Shopping list:
 
   * apples
   * oranges
   * pears
   
*   A list item.  
    With multiple paragraphs.

*   Another item in the list.
	* sublist item
		* subsublist item
 
## Ordered list
 Numbered list:
 
   1. apples
   2. oranges
   3. pears
   
 1. test
 2. Test2
 	
 	2.1 test3
 	
   
 
 The rain---not the reign---in
 Spain.
 
 
 Todo list :
 
 - [] checklist
 - [x] checked
 - [] checklist2

# Quote
 
> This is a blockquote.
> 
> This is the second paragraph in the blockquote.
>
> ## This is an H2 in a blockquote

# Code

Using quotes : I strongly recommend against using any `<blink>` tags.
	
	This is code using tab
	<?php echo $var; ?>
	</html>
	

# Escaping characters

Markdown provides backslash escapes for the following characters:

\   backslash  
`   backtick  
*   asterisk  
_   underscore  
{}  curly braces  
[]  square brackets  
()  parentheses  
\#   hash mark  
+   plus sign  
-   minus sign (hyphen)  
.   dot  
!   exclamation mark  

	
 
# Documentation
 
 [basics](http://daringfireball.net/projects/markdown/basics)
 
 