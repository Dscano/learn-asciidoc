# Introduction

This is intended to be a quick summary of changes to make from Madoko
markup, to AsciiDoc markup.


# Section headings

Section headings in Madoko are lines beginning with one or more
consecutive # characters.

They should be replaced in AsciiDoc with one more = character than
there were # characters, because a single = in AsciiDoc is used to
mark the title of the entire document.  Thus a "level 1 heading" line
in AsciiDoc begins with `==`, not `=`.


# Lists of items

Madoko:

```
- First item
- Second item
  * Sub-item
```

AsciiDoc:

```
* First item
* Second item
** Sub-item
```


# Bold text

Madoko: `**text to be bold here**`

AsciiDoc: `*text to be bold here*`
