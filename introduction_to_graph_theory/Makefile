TEXPROCESSOR := pdflatex
TEXFLAGS := -shell-escape

TARGET := graph_theory
SOURCES := $(wildcard *.tex)
SOURCES += $(wildcard chapters/*.tex)


all: $(TARGET).pdf clean

debug: $(TARGET).pdf


$(TARGET).pdf: $(SOURCES)
	$(TEXPROCESSOR) $(TEXFLAGS) main.tex &&\
		mv main.pdf $(TARGET).pdf


read: all
	evince $(TARGET).pdf &


clean:
	@-rm *.log 
	@-rm *.aux
	@-rm *.out 
	@-rm *.dvi 
	@-rm *.bbl 
	@-rm *.blg
	@-rm -r _minted*

cleanall: clean
	@-rm *.pdf


.PHONY: all read clean cleanall
