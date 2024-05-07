
SPEC=P4-16-spec

all: ${SPEC}.pdf ${SPEC}.html

#grammar.trimmed.mdk: grammar.mdk trim-madoko-comments.py
#	./trim-madoko-comments.py $< > $@

${SPEC}.pdf: ${SPEC}.adoc grammar.adoc
	asciidoctor-pdf -v $<

${SPEC}.html: ${SPEC}.adoc grammar.adoc
	asciidoctor -v $<

clean:
	/bin/rm -f ${SPEC}.pdf ${SPEC}.html
