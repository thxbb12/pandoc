FROM thxbb12/pandoc:2.6

RUN mkdir -p /pandoc/header
RUN mkdir -p /pandoc/bin
COPY header/slides_header.tex /pandoc/header
COPY header/labs_header.tex /pandoc/header
COPY bin/* /pandoc/bin/
RUN chmod +x /pandoc/bin/*

ENV PATH="/pandoc/bin:${PATH}"

CMD ["/pandoc/bin/help"]
