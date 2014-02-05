# The Makefile to automate building different versions of the book

all: web

really-all: web print html

web: main-web.tex
	xelatex main-web.tex
	biber main-web
	xelatex main-web.tex
	xelatex main-web.tex

print: main-print.tex
	xelatex main-print.tex
	biber main-print
	xelatex main-print.tex
	xelatex main-print.tex
	
html: png-drawings
	echo Not implemented
	echo FIXME xelatex -shell-escape

png-drawings:
	make -C drawings all
	
	

clean:
	rm -rf *.aux *.log *.fot *.blg *.bcf *.run.xml *.synctex.gz

clobber: clean
	rm -rf main-*.pdf

