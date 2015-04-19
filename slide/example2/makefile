FILENAME = ad_slide
TEX = $(FILENAME).tex
DVI = $(FILENAME).dvi
PDF = $(FILENAME).pdf


all:
	make tex
	make tex
	make dvipdf

distclean: clean
	make clean

clean: 
	rm *.aux *.dvi *.ilg *.ind *.log *.out *.toc *.nav *.snm *~

tex:
	platex $(TEX)

dvipdf:
	dvipdfmx $(DVI)

%.pdf: %.dvi
	dvipdfmx $<
