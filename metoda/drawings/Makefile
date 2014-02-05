# Makefile for standalone generated images
# On Windows Imagemagick 'convert' tool should be named 'imgconvert.exe' and be in %PATH%

SRC = $(wildcard *.tex)
DST = $(patsubst %.tex,%.pdf,$(SRC))
	
all: build

%.pdf:%.tex
	xelatex -shell-escape $<

build: $(DST)
	
clean:
	rm -rf *.pdf *.png  *.out *.log *.aux
