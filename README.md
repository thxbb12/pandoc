# pandoc

This repository is a collection of various pandoc related stuff.

- `examples/labs` contains examples of what can be achieved with pandoc to create practical labs along "correction" text embedded in the same original .md file.
	- To generate the PDF document, simply run `make` in that directory.

- `examples/slides` contains an example of somewhat nice looking slides created with pandoc. The generated PDF shows how various things can be accomplished with pandoc/latex/beamer.
	- To generate the PDF document, simply run `make` in that directory.

- dockerfiles contains (for now), two Dockerfiles:
	- pandoc: pandoc v2.6 image
	- md2pdf: image used to easily produce PDF files from .md documents
