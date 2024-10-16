SOURCE = $(wildcard *.tex)
PDF = $(patsubst %.tex,%.pdf,$(SOURCE))

%.pdf:%.tex
	xelatex -shell-escape -synctex=1 -interaction=nonstopmode $<

one: all
	pdftk slide-05-01.pdf slide-05-02.pdf slide-05-03.pdf slide-05-04.pdf slide-05-05.pdf cat output slide-05.pdf


.PHONY:all clean cleanall
all:$(PDF)

cleanall:
	rm -f *.pdf *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb *.bak *.org ~*

clean:
	rm -f *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb
