M - PDF generated from Madoko source
A - PDF generated from AsciiDoc source


Table of contents in A has level 4 and 5 headers, whereas M only has
headings up to level 3.  I like the extra headers in the table of
contents of A, personally, especially if that is one of the sections
you want to click on in a PDF reader to jump directly to it.

M has weird extra space in the TOC heading:

+ Operations on `error` types

I do not know why.  It is not in the M source.  This is better in A,
so nothing to do here.

In TOC of A, appendices have auto-lettered heading names like
"Appendix A", "Appendix B", etc.  Personally, that seems like a minor
improvement.

The entire A PDF is about 12 pages longer.  I am guessing this has to
do with a difference in font or vertical whitespace between elements.

A has extra vertical white space between items of a bulleted list.

All of these items are in the title page of M, but not of A.  TODO: I
would like to figure out how to make them appear in A:

+ version number
+ author
+ date
+ heading "Abstract"

In section 2, the first words in each bullet item are bolded in A, but
not in M.  The M markup has bold for those words, so I do not know why
it does not come out bold in M's PDF.  Seems better in A, without
further changes.

Sec 3: The word "target" in the sentence "generic term target for all
such devices" is italic in A, but not in M.  It has markup for
emphasis in M and A, so this seems better in A than M.

Cross-references show up as blue in xdg-open reader on Ubuntu on M, but 

Figure captions in A are left-adjusted, but centered-aligned in M.  I
prefere center-aligned, but do not know if there is a way to change
this in A.  TODO.

Figure captions in M have a horizontal rule line separating them from
the figure, but no such line in A.  TODO: Something to try to improve?

Figures in A appear wherever the markup for them does, relative to the
text.  They "float" in A, typically appearing at the top of a page.
TODO: It might be nice to change this in A, if there is a way.

Monospaced terms like `extern` are red in A, but black in M.  I do not
know if this is something people would prefer to change, or not.  It
seems reasonable to me.

Cross-references to an appendix in M appear as "Section B", but as
"Appendix B" in A.  I like A's better.

Paragraphs in A are separated by a line of vertical whitespace, and
have no indent on the first line of text.  No vertical whitespace
between paragraphs in M, and first line of text is indented.  TODO:
acceptable?

P4 code blocks in M have yellow background.  In A it is a light gray.
TODO: acceptable?  Easily changeable?

Pseudocode blocks in M have light blue background.  In A it is light
gray.  TODO: Easily changeable?
