M - PDF generated from Madoko source

A - PDF generated from AsciiDoc source, as of the version of AsciiDoc
  files in this repository as of this commit:

```bash
commit bd176c67645d3ded4b70077eff7a9be98cfa1d4e (HEAD -> main, origin/main, origin/HEAD)
Author: Andy Fingerhut <andy_fingerhut@alum.wustl.edu>
Date:   Sun Aug 4 19:25:19 2024 +0000
```

Logo on title page of A looks pretty nice.

M has date of revision on title page, but A does not.  Would be nice
to add this to A.

A has Abstract on a page by itself.  M has it on title page,
immediately followed on same page by table of contents.  Seems like an
acceptable difference to me.

A is about 13 pages longer than M, probably due to font and/or
vertical whitespace difference.  Seems reasonable to me.

Table of contents in A has level 4 and 5 headers, whereas M only has
headings up to level 3.  I like _very much_ the extra headers in the
table of contents of A, especially if that is one of the sections you
want to click on in a PDF reader to jump directly to it.  Example: See
sub-sections of 14.2.1 "Table properties" in A's TOC, which are absent
from M's TOC.

M has weird extra space in the TOC heading:

+ Operations on `error` types

I do not know why.  It is not in the M source.  This is better in A,
so nothing to do on A here.

In TOC of A, appendices have auto-lettered heading names like
"Appendix A", "Appendix B", etc.  That seems like a minor improvement.

A has extra vertical white space between items of a bulleted list.

In section 2, the first words in each bullet item are bolded in A, but
not in M.  The M markup has bold for those words, so I do not know why
it does not come out bold in M's PDF.  Seems better in A, without
further changes.

In A, each section starts on a new page, whereas in M new sections did
not force the start of a new page.  Seems like a minor acceptable
difference to me.

Sec 3: The word "target" in the sentence "generic term target for all
such devices" is italic in A, but not in M.  It has markup for
emphasis in M and A, so this seems better in A than M.

TODO: Cross-references show up as blue in xdg-open reader on Ubuntu on
M, but

In A PDF viewed in macOS Preview, cross-references to figures are
clickable links, displayed in a different color of text, whereas they
are not in M.  Seems like a minor improvement in A.

Figure captions in M have a horizontal rule line separating them from
the figure, but no such line in A.  Something to try to improve in A
output?  It does not seem like a bad difference to me.

Figures in A appear wherever the markup for them does, relative to the
text.  They "float" in A, typically appearing at the top of a page.
TODO: It might be nice to change this in A, if there is a way.

Monospaced terms like `extern` are red in A, but some dark color (dark
purple?) in M.  I do not know if this is something people would prefer
to change, or not.  It seems reasonable to me.

Cross-references to an appendix in M appear as "Section B", but as
"Appendix B" in A.  I like A's better.

Paragraphs in A are separated by vertical whitespace, and have no
indent on the first line of text.  No vertical whitespace between
paragraphs in M, and the first line of each paragraph is indented.
TODO: acceptable?

Color backgrounds of code blocks:

+ P4 code blocks, beginning [source,p4] in A

P4 code blocks in M have yellow background.  In A it is a light gray.
TODO: acceptable?  Easily changeable?

+ P4 pseudocode blocks, beginning [source,p4pseudo] in A

Pseudocode blocks in M have light green background.  In A it is light
gray.  TODO: Easily changeable?  Example: See pseudocode snippet at
end of Section 6.1.1 "Grammar".

+ grammar blocks, beginning [source,bison] in A

Grammar snippet text in M has light blue background.  In A it is light
gray.  TODO: Easily changeable?  Example: See grammar snippet in
Section 6.1.1 "Grammar".
