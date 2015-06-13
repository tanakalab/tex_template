FILENAME = template
#FILENAME = reference
TEX = $(FILENAME).tex
DVI = $(FILENAME).dvi
PDF = $(FILENAME).pdf


all:
	make tex
#bibtex を用いる場合は，下記の行のコメントアウトを取り除いて使用する
	#make pbibtex
	make tex
	make tex
	make dvipdf

distclean: clean
	make clean

clean: 
	rm *.bbl *.aux *.dvi *.ilg *.ind *.log *.out *.toc *~

tex:
	platex $(TEX)

pbibtex:
	pbibtex $(FILENAME)

dvipdf:
	dvipdfmx $(DVI)

%.pdf: %.dvi
	dvipdfmx $<
