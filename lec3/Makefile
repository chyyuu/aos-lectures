SOURCE = $(wildcard *.tex)
PDF = $(patsubst %.tex,%.pdf,$(SOURCE))

%.pdf:%.tex
	xelatex -shell-escape -synctex=1 -interaction=nonstopmode $<

one: all
	pdftk slide-03-01.pdf slide-03-02.pdf slide-03-03.pdf cat output slide-03.pdf


.PHONY:all clean cleanall
all:$(PDF)

cleanall:
	rm -f *.pdf *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb *.bak *.org ~*

clean:
	rm -f *.out *.toc *.aux *.log *.nav *.gz *.snm *.vrb
