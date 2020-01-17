FROM ubuntu:18.04

LABEL authors="Florent Gluck"

RUN apt-get update -y \
  && apt-get install -y --no-install-recommends \
    fontconfig \
    texlive-bibtex-extra \
    texlive-fonts-extra \
    texlive-fonts-recommended \
    texlive-latex-base \
    texlive-latex-extra \
    transfig \
    librsvg2-2 \
    wget python3 python3-pip \
	vim net-tools librsvg2-bin lmodern texlive-lang-french \
  && rm -rf /var/lib/apt/lists/*

RUN wget --no-check-certificate https://github.com/jgm/pandoc/releases/download/2.6/pandoc-2.6-1-amd64.deb && \
    dpkg -i pandoc* && \
    rm pandoc* && \
    apt-get clean
    
RUN pip3 install setuptools && pip3 install pandoc-latex-fontsize && pip3 install pandoc-numbering
    
RUN mkdir /src
VOLUME /src
WORKDIR /src

CMD ["pandoc" "-v"]
