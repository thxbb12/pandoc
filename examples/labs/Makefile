SRCS=$(wildcard *.md)
PDFS=$(SRCS:%.md=%.pdf)
PDFS_CORR=$(SRCS:%.md=%_corr.pdf)
UID=$(shell id -u)
GID=$(shell id -g)

doc: $(PDFS)

corr: $(PDFS_CORR)

all: doc corr

%.pdf: %.md
	docker run --user $(UID):$(GID) --rm --mount type=bind,src=$(PWD),dst=/src md2pdf build_lab $<

%_corr.pdf: %.md
	docker run --user $(UID):$(GID) --rm --mount type=bind,src=$(PWD),dst=/src md2pdf build_lab_corr $<

clean:
	rm -f $(PDFS) $(PDFS_CORR)

