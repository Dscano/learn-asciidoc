
SPEC=P4Runtime-Spec

ROUGE_STYLE=github
ROUGE_CSS= style

all: ${SPEC}.pdf ${SPEC}.html

${SPEC}.pdf: ${SPEC}.adoc
	time asciidoctor-pdf -a pdf-fontsdir=resources/fonts -v -r asciidoctor-mathematical -r asciidoctor-bibtex -a rouge-style=$(ROUGE_STYLE) $<

${SPEC}.html: ${SPEC}.adoc 
	time asciidoctor -v -r asciidoctor-mathematical -a rouge-css=$(ROUGE_CSS) $<

clean:
	/bin/rm -f ${SPEC}.pdf ${SPEC}.html resources/figs/stem-*.png
