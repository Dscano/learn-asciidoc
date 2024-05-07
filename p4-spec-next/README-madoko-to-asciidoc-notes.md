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

TODO: There are two numbered lists in the original Madoko version.  I
have tried to replace them with AsciiDoc auto-numbered lists like
these:

```
. First item
. Second item
```

but I keep seeing a message like this in the `asciidoctor` output for
such files.  How to correct this?

```
asciidoctor: WARNING: P4-16-spec.adoc: line 9205: unterminated listing block
```

TODO: The list in section "Operations on arbitrary-precision integers"
that has sub-bullets, followed by text at the original top level list
item level, is not parsed as desired by AsciiDoctor.  Learn how to do
this in AsciiDoc, if it is possible.

Answer: I found one answer on how to do this here:

+ https://docs.asciidoctor.org/asciidoc/latest/lists/continuation/#enclose-in-open-block


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

TODO: A few section names in the P4 spec are identical, e.g. at least
"keys" and "actions".  Learn how to reference a specific section even
when their names are identical.

TODO: Find all identically-named sections in the P4 spec, and give
them unique cross-reference tag names.


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

TODO: See if AsciiDoctor has a feature to avoid "widow lines",
i.e. only one or two lines of a block appearing on a page, when the
code block is split across multiple pages in PDF.


# Including text from part of a file, marked by tags

See here for how AsciiDoc specifies this:

+ https://docs.asciidoctor.org/asciidoc/latest/directives/include-tagged-regions/


# Tables

TODO: The markup is definitely different in Madoko and AsciiDoc.



# Footnotes

TOOD: Learn what the AsciiDoc way to describe footnotes is.


# Miscellaneous

TODO: In section "Operations on arbitrary-precision integers", an
occurrence of `<=` comes out as a different symbol, not the two
fixed-width symbols `<` followed by `=`, as desired.

TODO: In section "Operations on arbitrary-precision integers", there
are occurrences of LaTeX in-line math formulas like these that are not
rendering as desired.  Learn how to update them:

```
  The expression `a << b` is equal to $a \times 2^b$ while `a >> b`
  is equal to $\lfloor{a / 2^b}\rfloor$.
```


# Special characters

+ arrow pointing left and right with a single horizontal line between
  them, called `&harr;` in Madoko source.
  + Some old discussion here: https://discuss.asciidoctor.org/Double-Arrow-chars-td3918.html
  + Tried `&#8660;`.  Came out as an empty rectangle in PDF output.
  + Tried `&#x12d4;`.  Also came out as an empty rectangle in PDF output.


+ `&rarr;` in Madoko source, arrow pointing right only
  + See here: https://asciidoctor.org/docs/asciidoc-writers-guide/#replacements
  + Tried `&#8594;`.  Produced desired output in PDF output from AsciiDoctor.


Note that a hash mark `#` is used to enclose text to be highlighted.
If you want a literal hash mark in the output, or nearly any literal
text, enclose it in `+literal text without substitutions here+`, i.e.
start with a backtick followed by a plus sign, and end with a plus
sign followed by a backtick.

If you want literal text like this in Madoko source:

```
A list of `select`s
```

Where there is normal text immediately butting up against the
monospace text, then you must use double backticks surrounding the
monospace text in AsciiDoc, like shown below:

```
A list of ``select``s
```

TODO: The auto-numbering of section headings works for section numbers
3 levels deep, e.g. 2.3.4, but not further.  See if there is a global
setting that can increase this to 5 levels, which should be enough for
all sections that I know of in P4 language spec.