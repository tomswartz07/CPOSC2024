######################
#      Makefile      #
######################

filename=cposc2024

.PHONY: all clean-all pdf xe-pdf text view clean

all: pdf clean

clean-all:
	@rm -f ${filename}.{ps,log,aux,html,out,dvi,bbl,blg,snm,toc,nav,vrb}

pdf:
	pdflatex -halt-on-error -interaction=nonstopmode ${filename}
	# Run twice to update Table-of-Contents and other items
	pdflatex -halt-on-error -interaction=nonstopmode ${filename}

xe-pdf:
	xelatex -halt-on-error ${filename}

text: html
	html2text -width 100 -style pretty ${filename}/${filename}.html | sed -n '/./,$$p' | head -n-2 >${filename}.txt

html:
	@#latex2html -split +0 -info "" -no_navigation ${filename}
	htlatex ${filename}

# The following doesn't quite work as expected
#view:
#	while inotifywait --event modify,move_self,close_write ${filename}.tex; \
#		do \
#		pdflatex -halt-on-error -interaction=nonstopmode ${filename}; \
#		done

clean:
	$(RM) ${filename}.{ps,log,aux,html,out,dvi,bbl,blg,snm,toc,nav,vrb}
