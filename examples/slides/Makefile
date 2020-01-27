SRCS=$(wildcard *.md)
PDFS=$(SRCS:%.md=%.pdf)
UID=$(shell id -u)
GID=$(shell id -g)

all: $(PDFS)

%.pdf: %.md
	docker run --user $(UID):$(GID) --rm --mount type=bind,src="$(PWD)",dst=/src thxbb12/md2pdf build_slides $<

clean:
	rm -f $(PDFS)
