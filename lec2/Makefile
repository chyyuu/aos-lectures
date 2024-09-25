SOURCE = $(wildcard *.tex)
PDF = $(patsubst %.tex,%.pdf,$(SOURCE))

%.pdf:%.tex
	xelatex -shell-escape -synctex=1 -interaction=nonstopmode $< 

one: all
	pdftk slide-02-01.pdf slide-02-02.pdf slide-02-03.pdf slide-02-04.pdf slide-02-05.pdf slide-02-06.pdf slide-02-07.pdf cat output slide-02.pdf

.PHONY:all clean cleanall
all:$(PDF)

cleanall:
	rm -f *.pdf *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb *.bak *.org ~*

clean:
	rm -f *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb
