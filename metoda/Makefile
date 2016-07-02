# Build the book
# A single PDf target is preserved

all: main-web.pdf

CHAPTERS = applications afterword cycle interpretation parallel alternatives bt lang fullplatform paravirt caches traces contrib ic-route state overview virt

main-web.pdf: main-web.tex *.tex
	xelatex main-web.tex
#	biber main-web
        # chapterbib requires execution of bibtex for every individual chapters
	for chap in $(CHAPTERS); do bibtex $$chap; done
	xelatex main-web.tex
	xelatex main-web.tex

clean:
	rm -rf *.aux *.log *.fot *.blg *.bcf *.run.xml *.synctex.gz *.bbl *.backup *.out *.toc

clobber: clean
	rm -rf main-*.pdf
