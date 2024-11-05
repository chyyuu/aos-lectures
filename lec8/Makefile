SOURCE = $(wildcard *.tex)
PDF = $(patsubst %.tex,%.pdf,$(SOURCE))

%.pdf:%.tex
	xelatex -shell-escape -synctex=1 -interaction=nonstopmode $<

one: all
	pdftk slide-08-01.pdf slide-08-02.pdf slide-08-03.pdf slide-08-04.pdf slide-08-05.pdf cat output slide-08.pdf


.PHONY:all clean cleanall
all:$(PDF)

cleanall:
	rm -f *.pdf *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb *.bak *.org ~*

clean:
	rm -f *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb
