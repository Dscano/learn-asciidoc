
SPEC=P4-16-spec

ROUGE_STYLE=igorpro

all: ${SPEC}.pdf ${SPEC}.html

grammar.trimmed.adoc: grammar.adoc trim-asciidoc-tag-comments.py
	./trim-asciidoc-tag-comments.py $< > $@

${SPEC}.pdf: ${SPEC}.adoc grammar.adoc grammar.trimmed.adoc
	time asciidoctor-pdf -v -r asciidoctor-mathematical -a rouge-style=$(ROUGE_STYLE) $<

${SPEC}.html: ${SPEC}.adoc grammar.adoc grammar.trimmed.adoc
	time asciidoctor -v -r asciidoctor-mathematical -a rouge-style=$(ROUGE_STYLE) $<

clean:
	/bin/rm -f ${SPEC}.pdf ${SPEC}.html grammar.trimmed.adoc
