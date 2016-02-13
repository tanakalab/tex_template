FILENAME = example
TEX = $(FILENAME).tex
DVI = $(FILENAME).dvi
PS = $(FILENAME).ps
PDF = $(FILENAME).pdf


all:
	make tex
	make dvips
	make ps2pdf

distclean: clean
	make clean

clean: 
	rm *.aux *.dvi *.ilg *.ind *.log *.out *.toc *.nav *.snm *~

tex:
	platex $(TEX)

dvips:
	dvips $(DVI)

ps2pdf:
	ps2pdf $(PS)

dvipdf:
	dvipdfmx $(DVI)

%.pdf: %.dvi
	dvipdfmx $<
