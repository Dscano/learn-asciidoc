FNAME=trybibtex

all: $(FNAME).pdf $(FNAME).html

$(FNAME).pdf: $(FNAME).adoc
	asciidoctor-pdf -v -r asciidoctor-bibtex $<

$(FNAME).html: $(FNAME).adoc
	asciidoctor -v -r asciidoctor-bibtex $<

clean:
	/bin/rm -f $(FNAME),pdf $(FNAME).html
