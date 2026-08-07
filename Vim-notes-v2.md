# Vi, Vim, Neovim and OpenVim notes version 2

>ekine 2026  

Vim has two basic modes *insert mode* triggered with the *i* key; in which you wite text as if in any normal text editor.
Another is *normal mode*, which provides efficient ways to navigate and manipulate text, *Esc* key.

Pressing the *Esc* key alternating with *i* changes from *normal mode* to *insert mode*.
Usually you can see wich mode is enabled in the lower or upper part of a terminal or editor.

The third mode is *visual mode*, in this mode you can select text with the cursor before you decide what to do with it.

## Basic movement
The letters *h*, *j*, *k* and *l* are used in similar way as the arrow keys (left, down, up and right; in that order).

According to some Vim tutorials, arrow keys are not always supported as movement.
In my experience all the terminal applications that I have used support this feature.  I'm sure there is hardware and embbeded systems where this feature is a life saver,
 can be used to program macros and probably when the navigation is fully comprehended and executed can wildly increase the writing and edit speed.

### Words
To navigate in terms of words the key *w* moves the cursor to the start of the next word;
*e* moves it to the end of the word; and *b* moves to the beginning of a word.

This is similar on how *ctrl + arrow keys* work in other text processors like MS's Word or Libreoffice's Writter.

## Number powered movement
Moving is not limited to individual keys; you can combine movement keys with a number, *3w* is the same as pressing the key *w* three times.  
> syntax: number + navigation key

Notes: *w* and *b* stop when facing some operator symbols, probably considers them as delimiters or word separators.  
* *\.* dot 
* *\-* hypen 
* *\** asterisk 

## Structured text
In text structured with parentheses *\(* *\)*, curly braces *\{* *\}* or brackets *\[* *\]* use the percentage symbol *\%* to jump to the matching symbol.

## Number powered text insert
Text can be inserted multiple times, for example an underline consisting of ten hypens can be places with the command *30i-Esc* in normal mode.  
> syntax: number i - Esc

I tested with more than one thousand lines.

## Find characters
To find and move to the next or previous ocurrence of a search use lowercase *f* and upper case *F*.
It can be combined with numbers, for exampe *3f*.

This works only for letters.

## Find words
To find words or sentences use a slash *\/* with the word and use lowercas *n* for the next concurrence and uppercase *N* for the previous one. It can look for phrases and words, is by default case sensitive (distincts lower form uppercase).  
> *2fé* looks for the second *é*
> */the lion* looks for the phrase


If the word is already selected with the cursor, use \* to find the next match and use *\#* for the previous one.  
Is also possible to look for concurrences including just the last or first part of a word.  
> Syntax: / \\< word \\>  
search command + beginning of a word + word + end of a word

> /\\<car  carreta
> /car\\>  sacar

### Case sentitive in searches
To override case sensitive searches of use a backlash plus c *\\c*.  
> /Gnu\\c  to look for GNU, Gnu and gnu 

It is possible to highlight all matches, clear highlights and ignore cases using *set* options.  
> :set ignorecase  
to ignore case sensitive searches  

> :set hlsearch  
to highlight matches  

> :noh  
to clear highlights


## Backwards search  
Searches can be done from the end of the document to the beggining using the question mark *\?* instead of a slash *\/*.

## Search for only one word
> /\\<word\\>  
search + beginning of a word + end of a word

## Find and replace
The search and replace is done with the *:substitute* command, often abreviated as *:s*.

The basic syntax is as followed:  
> :\[range\]s/\{pattern\}/\{replacement\}/\[flags\] \[count\]

* range, wich lines to apply the command to.
* pattern, the text or regular expression to search for.
* replacement, the text to replace with.
* flags, options that change how the commands behave.
* count, a positive integer that multiplies the command.

First match in current line.  
> :s/ski/sky

All matches in current line, with global *g* flag.  
> :s/ski/sky/g

Delete all matches.  
> :s/Privatekey999//g

Pipes \|, can be used to separate or  as delimiters, the flag *c* forces to confirmate.

To replace in line numbers as a range, fe. to subsititute all ocurrences in lines 5 to 10:  
> :5,10s/ski/sky/g

## Go to line
The keys *gg* take you to the beginning og the file, *G* sends you to the end.

To go to a specific line, give the line number plus uppercase *G*.  
> 2G

## Go to last edit and marks
* ma - set mark a
* \'a - jump mark a
* :marks - lists all marks
* \'. - jump last edit line
* \'\' - jump last position

## Insert a new line
To insert a new line after the cursor use lower case *o*, user upper case *O* to add a line before the cursor. After a new line is created the editor will set to *insert mode*.

## Removing, replacing and delete
Lower case *x* delete the character under the cursor; upper case *X* delete the character to the left of the cursor (similar to the *back* key).

To replace only one character under the cursor use the key *r*, uppercase *R* sets the editor in *replace mode*.

The delete command is *d*. It can be combined with movement, *dw* deletes the first word in front of the cursor and *db* the word before the cursor.  
The delete command also copies the content, that can be pasted with *p* in other place of the document. To delete two words user *d2w*. The command *dd* deletes a line and uppercase *D* deleted everything in from the cursor to the end of the line.

## Paste and yank commands
The key *y* is the copy or yank command, *yy* copies a line, *y\$* copies to the end of a line.  
The key *p*, inserts the content copied by the yank or delete commands, lowercase *p* paste after cursor and uppercase *P* paste befor the cursor.

## Repetition
To repeat previous command use the dot key *\.*, it stores the last used command and can be run until a new one is store.

## References  
* Fellman, Nathan (2009). *Stackoverflow: Searching a word in Vim*.

    * <https://stackoverflow.com/questions/458915/searching-word-in-vim>

* Markdown Viewer (2009). *Markdown Viewer*.  

    * <https://markdownviewer.org/>

* OpenVim.com (2026). *Find a character, f and F*.
   
    * <https://openvim.com>

* Panivski, Dejan (2026). *How to search in Vim/Vi*.

    * <https://linuxize.com/post/vim-search/#search-highlighting>

* Panivski, Dejan (2026). *Vim Cheatsheet*.

    * <https://linuxize.com/cheatsheet/vim/>

* Panivski, Dejan (2026). *Find and replace in Vim/Vi*.

    <https://linuxize.com/post/vim-find-replace/>
