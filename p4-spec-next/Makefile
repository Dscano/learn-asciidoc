
SPEC=P4-16-spec

all: ${SPEC}.pdf ${SPEC}.html

#grammar.trimmed.mdk: grammar.mdk trim-madoko-comments.py
#	./trim-madoko-comments.py $< > $@

${SPEC}.pdf: ${SPEC}.adoc
	asciidoctor-pdf $<

${SPEC}.html: ${SPEC}.adoc
	asciidoctor $<

clean:
	/bin/rm -f ${SPEC}.pdf ${SPEC}.html
