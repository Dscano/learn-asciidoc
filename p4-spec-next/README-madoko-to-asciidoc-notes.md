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

Put this in the document heading in AsciiDoc to enable section numbering:

```
:sectnums:
```


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


# Emphasis

Madoko: `_underscore around a word or phrase_`

AsciiDoc: The same!


# Monospace

Madoko: enclose text within backticks

AsciiDoc: The same!


# Subscript and Superscript

Madoko: `P4~16~` for subscript of the `16`, and `P4^T^` for superscript of the `T`.

AsciiDoc: The same!  No change needed!


# Figure

TODO: Add notes on how to control size of inserted figure.

AsciiDoc:
```
.Caption goes here on one line.
[#fig-tag-for-cross-references]
image::filename.png[]
```


# Figure cross-reference

Madoko:
```
Figure [#fig-tag-for-cross-reference]
```

AsciiDoc:

```
<<fig-tag-for-cross-reference>>
```


# Section cross-reference

Madoko section heading with cross-reference tag name:

```
# Appendix: P4 reserved keywords { #sec-p4-keywords }
```

Madoko cross-reference to that section:
```
Appendix [#sec-p4-keywords]
```

Madoko section heading, NO cross-reference tag name required, as one
is automatically generated from the section name:

```
== Appendix: P4 reserved keywords
```

AsciiDoc cross-reference to that section.  Note the leading `_`,
blanks replaced with `_`, and I believe all non-alphanumeric
characters omitted:

```
<<_appendix_p4_reserved_keywords>>
```

If you are not sure, look in the output of `asciidoctor` runs to see
if there are any warning messages about `possible invalid reference`.


# em dash

Madoko: `---`

AsciiDoc: TODO


# automatic P4_16 code syntax colorization in code blocks

Madoko: solved problem

AsciiDoc: TODO



# Code blocks with syntax highlighting

Madoko:

```
~ Begin P4Example
control MatchActionPipe<H>(in bit<4> inputPort,
                           inout H parsedHeaders,
                           out bit<4> outputPort);
~ End P4Example
```

The above required special definition in the header for a `P4Example`
block.

```
[source,ruby]
----
code block goes here
----
```

TODO: Read AsciiDoc docs on how to enable syntax highlighting for P4:

+ https://docs.asciidoctor.org/asciidoc/latest/verbatim/source-blocks/

TODO: In Section 6.1 "Very Simple Switch Architecture" there are some
list items with code blocks embedded in the middle of text, and there
was a special syntax in Madoko to make the text after the code block
indented inside the list item as the text before the code block was.
I do not yet know how to do that in AsciiDoc, if it provides a way.
In Madoko, such lines consist of only the backslash character `\`.
