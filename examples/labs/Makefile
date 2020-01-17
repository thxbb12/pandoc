INPUTS=$(wildcard *.md)
OUTPUTS=$(INPUTS:%.md=%.pdf)
OUTPUTS_CORR=$(INPUTS:%.md=%_corr.pdf)
UID=$(shell id -u)
GID=$(shell id -g)

all: $(OUTPUTS) $(OUTPUTS_CORR)

# pandoc -t beamer $< -o $@ -V theme:$(THEME) --pdf-engine=pdflatex --slide-level 2 -H header.tex --listings

%.pdf: %.md
	docker run --user $(UID):$(GID) --rm --mount type=bind,src=$(PWD),dst=/src md2pdf build_lab $<

%_corr.pdf: %.md
	docker run --user $(UID):$(GID) --rm --mount type=bind,src=$(PWD),dst=/src md2pdf build_lab_corr $<

clean:
	rm -f $(OUTPUTS) $(OUTPUTS_CORR)
