INPUTS=$(wildcard *.md)
OUTPUTS=$(INPUTS:%.md=%.pdf)

all: $(OUTPUTS)

# pandoc -t beamer $< -o $@ -V theme:$(THEME) --pdf-engine=pdflatex --slide-level 2 -H header.tex --listings

%.pdf: %.md
	docker run --rm --mount type=bind,src=$(PWD),dst=/docs thxbb12/pandoc:2.6 pandoc -t beamer /docs/$< -o /docs/$@ --pdf-engine=pdflatex -H /docs/header/header.tex --listings --filter pandoc-latex-fontsize --filter pandoc-numbering

clean:
	rm -f $(OUTPUTS)
