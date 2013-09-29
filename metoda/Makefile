# FIXME This makefile does not work!

LATEXCOMMAND=xelatex
BIBTEXCOMMAND=bibtex8
OPTIONS= -halt-on-error

TEXFILE=main.tex
LOGFILE=main.log

all: main.pdf

firstpass:
	bash -c "while ( $(LATEXCOMMAND) $(OPTIONS) $(TEXFILE) ; grep -q 'Rerun to get cross' $(LOGFILE) ) do true ; done"

	# $(BIBTEXCOMMAND) `basename $< .aux`;
    
bibtexing: chap*.aux
	$(BIBTEXCOMMAND) `basename $^ .aux`
	bash -c bibtex.sh

main.pdf: $(TEXFILE) firstpass bibtexing firstpass

clean: 
	rm -rf *.aux *.fot *.lof *.lot *.out *.backup *.toc *.log *.tmp *.idx *.ind  *.bbl

