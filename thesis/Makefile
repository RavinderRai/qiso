# Sample Makefile
# $Id: Makefile 387 2012-11-12 15:11:48Z vlado $

THESIS_NAME=thesis

help:
	@echo make all

.PHONY: all

all:
	latex $(THESIS_NAME).tex
	latex $(THESIS_NAME).tex
	bibtex $(THESIS_NAME)
	latex $(THESIS_NAME)
	dvips -t letter thesis.dvi -o thesis.ps
	pdflatex thesis.tex

body:
	latex $(THESIS_NAME).tex

glossary:
	latex $(THESIS_NAME).tex
	makeindex -s $(THESIS_NAME) -o $(THESIS_NAME).gls $(THESIS_NAME).glo

bibliography:
	latex $(THESIS_NAME).tex
	bibtex $(THESIS_NAME)

clean:
	-rm *.dvi *.aux *.bbl *.blg *.log *.toc *.lof *.lot *.glo *.gls *.ist *.ilg *.ps *.out

spotless: clean
	-rm *.pdf

