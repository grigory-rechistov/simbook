# Build the book
# A single PDf target is preserved

all: main-web.pdf

main-web.pdf: main-web.tex *.tex
	xelatex main-web.tex
	biber main-web
	xelatex main-web.tex
	xelatex main-web.tex

clean:
	rm -rf *.aux *.log *.fot *.blg *.bcf *.run.xml *.synctex.gz *.bbl *.backup *.out

clobber: clean
	rm -rf main-*.pdf
