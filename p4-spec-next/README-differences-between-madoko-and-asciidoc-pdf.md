This comparison has been updated to version 1.2.5

M - PDF generated from Madoko source of version 1.2.5 of the language spec

A - PDF generated from AsciiDoc source, as of the version of AsciiDoc
  files in this repository as of the latest commit made on 2024-Oct-13

Logo on title page of A looks pretty nice.

TODO: M has date of revision on title page, but A does not.  Would be
nice to add this to A.

M has abstract on first page.  A has abstract after the table of
contents, just before the first section of the contents.  Seems like a
reasonable difference to me.

M is 189 pages.  A is 176 pages.  Probably due to font and/or vertical
whitespace difference.  It might also be due to smaller top, bottom,
left, and right margins in A than there are in M.  Seems reasonable to
me.

Table of contents in A has level 4 and 5 headers, whereas M only has
headings up to level 3.  I like _very much_ the extra headers in the
table of contents of A, especially if that is one of the sections you
want to click on in a PDF reader to jump directly to it.  Example: See
sub-sections of 14.2.1 "Table properties" in A's TOC, which are absent
from M's TOC.

M has weird extra space in the TOC heading:

+ 8.2 Operations on `error` types

I do not know why.  It is not in the M source.  This is better in A,
so nothing to do on A here.

In TOC of A, appendices have auto-lettered heading names like
"Appendix A", "Appendix B", etc.  That seems like a minor improvement.

A has extra vertical white space between items of a bulleted list.
Seems like a reasonable difference to me.

In section 2, the first words in each bullet item are bolded in A, but
not in M.  The M markup has bold for those words, so I do not know why
it does not appear bold in M's PDF.  Seems better in A, without
further changes.

In A, top-level section sometimes start on a new page, even if it
leaves up to about 1/2 a page empty at the end of the previous
top-level section.  In M, I believe this never occurs.  Seems like a
minor acceptable difference to me.

Sec 3: The word "target" in the sentence "generic term target for all
such devices" is italic in A, but not in M.  It has markup for
emphasis in M and A, so this seems better in A than M.

In A, cross-references to sections and figures show up as clickable
blue links on several PDF readers I have checked, including:

+ evince on Ubuntu Desktop Linux
+ Preview on macOS 14.6.x

This does not occur for cross-references in M.  Seems like a minor
improvement in A.

TODO: In M, cross-references to a top-level section are "Section
<number>".  In A they are "Chapter <number>".  In A they are "Section
<number.number>" if it is a second level or lower level section.
Acceptable?

Figure captions in M have a horizontal rule line separating them from
the figure, but no such line in A.  Something to try to improve in A
output?  It does not seem like a bad difference to me.  In addition, A
has figure captions in Italic font, but not Italic in M.

Figures in A appear wherever the markup for them does, relative to the
text.  They "float" in A, typically appearing at the top of a page.
TODO: It might be nice to change this in A, if there is a way.

Monospaced terms like `extern` are red in A, but some dark color (dark
purple?) in M.  I do not know if this is something people would prefer
to change, or not.  It seems reasonable to me.

TODO: Second and third level bullet symbols in bullet lists of A
appear as rectangular black-lined boxes with white interior in PDF
output.  In M, second level bullets appear as dashes, and third level
as asterisks.  It would be nice to improve this in A.  Example: See
second bullet list in Section 3.  For third level bullet, see second
bullet list in Section 6.8.

Cross-references to an appendix in M appear as "Section B", but as
"Appendix B" in A.  I like A's better.

Paragraphs in A are separated by vertical whitespace, and have no
indent on the first line of text.  No vertical whitespace between
paragraphs in M, and the first line of each paragraph is indented.
Both seem quite readable to me.

Color backgrounds of code blocks:

+ P4 code blocks, beginning [source,p4] in A source

P4 code blocks in M have yellow background.  In A it is a light gray.
TODO: acceptable?  Easily changeable?

+ P4 pseudocode blocks, beginning [source,p4pseudo] in A source

Pseudocode blocks in M have light green background.  In A it is light
gray.  TODO: Easily changeable?  Example: See pseudocode snippet at
end of Section 6.1.1 "Grammar".

+ grammar blocks, beginning [source,bison] in A source

Grammar snippet text in M has light blue background.  In A it is light
gray.  TODO: Easily changeable?  Example: See grammar snippet in
Section 6.1.1 "Grammar".

TODO: Footnotes in M appear at the bottom of the page where the
footnote superscript [1], [2], etc. appears.  Footnotes in A appear at
the bottom of the last page of the section where the footnote
superscript appears, perhaps several pages later.  It would be nice to
change this if possible.

TODO: Tables look a bit different between A and M.  I like the visual
style of M a bit better, but do not know how to improve A's PDF output
here.
