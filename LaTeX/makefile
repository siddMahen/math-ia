# VIEWER and DOC set by parent makefile

render: build
	open -a $(VIEWER) $(DOC).pdf

build:
	latex -shell-escape $(DOC)
	bibtex $(DOC)
	latex -shell-escape $(DOC)
	pdflatex -shell-escape $(DOC)

clean:
	rm $(DOC).aux
	rm $(DOC).dvi
	rm $(DOC).log
	rm $(DOC).out

.PHONY: build render
