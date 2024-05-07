This directory contains the beginnings of an experiment to convert the
Madoko source of the P4-16 language specification into AsciiDoc
format.

The file `P4-16-spec.mdk` is the particular version of the Madoko
(https://www.madoko.net) source file that is being experimented with,
and `P4-16-spec.adoc` is very similar, but with many small differences
to make it use AsciiDoc markup (https://asciidoc.org).


# Markup version

Files:
- ```P4-16-spec.adoc``` is the main file.
- ```grammar.mdk``` is the whole grammar in a single file included at
  the end of the main file. TODO: the intent is to include grammar
  fragments from this file in the different sections using the INCLUDE
  directive with labeled fragments. I didn't yet find a nice way to
  discard the labels and have this work satisfactorily.
- ```p4.json``` is providing custom syntax highlighting for P4. It is a rip
  off from the cpp.json provided by Madoko (the "extend" clause does
  not work, my version of Madoko asks for a "tokenizer" to be
  defined). Style customization for each token can be done using CSS
  style attributes (see token.keyword in line 20 of ```P4-16-spec.mdk```).
- ```figs/*.png``` exported figures from the P4-16-draft-spec.pptx
- ```Makefile``` builds documentation in the build subdirectory


## Building

Follow the instructions for various platforms below.

HINT: For *nix builds using make, you can use use `make
P4-16-spec.html` for quicker turnarounds and `make` for the final
html + PDF output.


### MacOS

TODO


### Linux

Use the Bash script
[`install-asciidoctor.sh`](../bin/install-asciidoctor.sh) to install
AsciiDoctor on an Ubuntu system.


### Windows

TODO
