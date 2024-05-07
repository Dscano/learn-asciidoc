
SPEC=P4-16-spec

#all: ${SPEC}.pdf ${SPEC}.html
all: ${SPEC}.pdf

grammar.trimmed.adoc: grammar.adoc trim-asciidoc-tag-comments.py
	./trim-asciidoc-tag-comments.py $< > $@

${SPEC}.pdf: ${SPEC}.adoc grammar.adoc grammar.trimmed.adoc
	asciidoctor-pdf -v $<

${SPEC}.html: ${SPEC}.adoc grammar.adoc grammar.trimmed.adoc
	asciidoctor -v $<

clean:
	/bin/rm -f ${SPEC}.pdf ${SPEC}.html grammar.trimmed.adoc
