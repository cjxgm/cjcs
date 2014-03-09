<!-- vim: set ts=4 sw=4 sts=0 noet ft=markdown : -->
# clanjor coding style

<hr>
## general
these rules apply to anything.

### anti-uppercase-ism
no uppercase letters are allowed unless explicitly stated.

### vim modeline
whether you use vim or not, always put vim modeline at the
very beginning of the file. usually you put it on the first line,
but if there is a shebang line, put the modeline after it.

the vim modeline *must* contain:
```vim
set ts=4 sw=4 sts=0 noet
```

for example, the modeline of this document is:
```html
<!-- vim: set ts=4 sw=4 sts=0 noet ft=markdown : -->
```
it's the first line of this document.

and in c code:
```c
// vim: ts=4 sw=4 sts=0 noet
```

### no nonsense bytes
* don't put modeline of any other editors.
* never contain blanks at the end of line, use this to detect them:
```vim
func! HighlightExtraSpace()
	syn match ExtraSpace "\s\+$"
	hi def link ExtraSpace Error
endfunc
au BufNewFile,BufRead * call HighlightExtraSpace()
```

### abbreviation
abbreviations are encouraged. use common linux abbreviations whenever
possible, e.g. `rm` for `remove`, `dup` for `duplicate`.
but *don't overdo this*!

### blanks
spaces` `, tabs`\t` and newlines`\n` are blanks. returns`\r` are not.
returns are not allowed to be in the code.

### indentation
*tabs only*. tabs must be *4-space wide*.
identation should generally obey to the vim's auto-indent and smart-indent.

### tabular
spaces only.

### blank line
### zen of comment
before writing any "comment", ask yourself:
* can i just put a blank line to make things clear?
* is there any specific rule that force me to add that comment?
* can i refactor everything to remove the comment?

**blank lines are the best comments.**

never write in-code documents.

### optimize first
### speed matters
### size matters
### push to edge
### nocompatible


<hr>
## lua specific

### anti-uppercase-ism
no capital letter is allowed in lua code.
### module
### quote
### identifier

<hr>
## c specific
### anti-uppercase-ism
* only types can be camel-cased.
* only macros can be fully-capitalized.
* any other identifiers must be in lower\_case

### identifier

### gcc only

<hr>
## markdown specific

