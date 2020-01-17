INPUTS=$(wildcard *.md)
OUTPUTS=$(INPUTS:%.md=%.pdf)
UID=$(shell id -u)
GID=$(shell id -g)

all: $(OUTPUTS)

# pandoc -t beamer $< -o $@ -V theme:$(THEME) --pdf-engine=pdflatex --slide-level 2 -H header.tex --listings

%.pdf: %.md
	docker run --user $(UID):$(GID) --rm --mount type=bind,src=$(PWD),dst=/src md2pdf build_slides $<

clean:
	rm -f $(OUTPUTS)
