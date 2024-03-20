FROM alpine:latest

RUN apk add --no-cache \
make \
texinfo \
texlive \
texlive-xetex \
texmf-dist \
texmf-dist-most \
texmf-dist-formatsextra

WORKDIR /data
VOLUME ["/data"]

# docker build . -t latex:latest
# docker run --rm -v $(pwd):/data latex:latest pdflatex cposc2024.tex
# OR
# docker run --rm -v $(pwd):/data latex:latest make all
