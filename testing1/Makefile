all: trybibtex.html trybibtex.pdf

trybibtex.html: trybibtex.adoc
	asciidoctor -r asciidoctor-bibtex $<

trybibtex.pdf: trybibtex.adoc
	asciidoctor-pdf -r asciidoctor-bibtex $<
