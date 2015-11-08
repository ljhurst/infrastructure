################################################################################
################################################################################
######################## Makefile for Latex Documents ##########################
################################################################################
################################################################################

XEX = xelatex

SOURCE_FILES = $(wildcard *.tex)
PDFS = $(SOURCE_FILES:%.tex=%)

TEMPLATES = $(wildcard templates/*.tex)
TEMPPDFS = $(TEMPLATES:%.tex=%)

.PHONY: clean

release: $(PDFS)

template: $(TEMPPDFS)

%: %.tex
	$(XEX) $^

open: $(PDFS)
	gnome-open *.pdf
clean:
	$(RM) *.log *.aux *.out
