# Markdown: use and notes
>ekine 2026  

### About markdown (files .md)

Markdown, extension .md, is a lightweight markup language for creating formatted text using a plain text editor.  
Due ambiguities using in the original release, in 2014 long-standing contributtors released **Commonmark**.  
Is considered a "true structurated text format" to optionally be converted to xhtml or html.

One key goal is readability unlike heavier markup languages as *rft* or *html*.


## Basic syntax

### Headings  
To create a heading adda number sign in front of a word or a phrase. I goes from one to six levels descending.  
For example:

* \# Header = level one "Header"
* \## Header = level two "Header"
* \### Header = level three "Header"

An alternate syntax consists in add any number of the equal sign *\=* or hypen *\-* for headings of level one and two (this exists probably for readability only).


### Paragraphs  
To create paragraphs just use blank lines and to breate a break just use two spaces and a blankline.

* space + space + break = New line
* break + break = \<br\> (html entity)

### Emphasis
To bold text or phrases add two asterisks or underscores without spaces.

* \*\*bold text\*\*
*  \_\_bold text\_\_
* **bold text**

Some applications don't agree on the use of underscores, so use asterisks for compatibility.

### Italic
To italicize text add one asterisk of underscore to a word or phrase.

* \*italicized word\*
* *italicized word*

Markdown application do not agree on how to use underscores in the middle of a word, use asterisks for compatibility.

### Underline

Apparently to underscore a word or a phrase, add a tilde at the begining and the end of the text.

*  \`underscore\`
* `underscore`

### Blockquotes
To create a blockquote add a *more than* sign or an *opening angle bracket* in front of a paragraph. This is not compatible wwith wordgrinder.

* \>Dorothy followed her.
* >Dorothy followed her

#### Blockquotes with multiple paragraphs
Blockquotes can contain multiple paragraphs.  
Add an *opening angle bracket* on the black lines between paragraphs.

* \>Dorothy followed her.
* \>
* \>Yes.


> Dorothy followed her.
> 
> Yes.

### Notes
Indented lists, lines, tables, nested blockquotes, hyper links, comments, alignments and most of html entities are no available in wordgrinder.

### Horizontal rules
To create a horizontal rule, use three of more asteriks, dashes or underscores on a line by themselves.  
For compatibility put them in backticks.

* blank
* \_\_\_
* blank


---

### Code
To denote a word or phrase as code enclose it in backticks \`.  

Codeblocks are normally idented four spaces or one tab.

* \`apt-cache search wordgrinder

`apt-cache search wordgrinder`

### Links
To create a link, enclose the link in brackets and then follow immediatly th URL in parentheses.

* My favourite browser is \'[ Duckduckgo \'] \'( https://noia.duckduckgo.com \')

* My favourite browser is [Duckduckgo](https://noia.duckduckgo.com)


### URLs and email
To quickly turn an URL or email addresses into a link, enclose it in brackets.

* \< https://www.markdownguide.com \>
* <https://www.markdownguide.com>

Markdown applications don't agree on how to use spaces. For compatibility use %20 for spaces, %28 for opening parenthesis and %29 for closing parentheses.

### Html
Many markdown applications use html tags in markdown-formatted text.  
This is helpfful to change attributes of an element. For security reasons not all markdown application support html, in doubt check each application's documentation.

Use blank line to separate html elements, tabs and spaces interfere with formatting. Is nor possible to use Markdown syntax inside block level tags.

### For spanish tildes and ling&uuml;istics
Use html signs aka entities.

* &aacute; = \&aacute\;
* &eacute; = \&eacute\;
* &iacute; = \&iacute\;
* &oacute; = \&oacute\;
* &uacute; = \&uacute\;


* &auml; = \&auml\;
* &euml; = \&euml\;
* &iuml; = \&iuml\;
* &ouml; = \&ouml\;
* &uuml; = \&uuml\;

* &ecaron; = \&ecaron\;
* &ecirc; = \&ecirc\;
* &edot; = \&edot\;
* &egrave; = \&egrave\;
* &emacr; = \&emacr\;


### Escaping characters
To display a character that would otherwise be used to format text in Markdown, add a blacklash in front of the character.

* \\ backlash
* \` backtick
* \* asterisk
* \_ underscore
* \{\} curly braces
* \[\] brackets
* \<\> angle brackets
* \(\) parentheses
* \# pound sign 
* \+ plus sign
* \- minus sign (hypen)
* \. dot
* \! exclamation mark
* \| pipe


### Indentation
Indentation in paragraphs is not supported by Markdown.  
An alternative is to use the  html's *non breacking space* entity.

* \&nbsp

### Comments
Comments are invisible text not printable. Markdown does not support comments but this is a solution: use brackets opening + comment +bracket closing + colon + space + pound sign.

* \'[ comment \']\: \'#

This is not possible in wordgrinder.

### Tables
Tables are not stable and constantly failing. To add a table, use three or more hypens to create each column header, and use pipes to separate each column.

* \| Syntax \| Description \|
* \| \-\-\- \| \-\-\- \|
* \| header \| title \|
* \| paragraph \| text \|

| Syntax | Description |
| --- | --- |
| header | title |
| paragraph | text|

Some applications allow to use html tags to get spaces inside "cells" \<br\>.

## References

 Gruber, John (2026). *Markdown*.  
<https://daringfireball.net/projects/markdown/>


 Markdownguide (2026). *Basic syntax*.  
<https://www.markdownguide.org/basic-syntax/> 


 Markdownguide (2026). *Extended syntax*.  
<https://www.markdownguide.org/extended-syntax/>

 Markdownguide (2026). *Hacks*.  
<https://www.markdownguide.org/hacks/#comments>

 Openvim (2026). *Visual mode*.  
<https://openvim.com/>

 Wikipedia (2026). *Markdown*.  
<https://en.wikipedia.org/wiki/Markdown>

 W3schools (2026). *Html entities*.  
<https://www.w3schools.com/charsets/ref_html_entities_e.as>
