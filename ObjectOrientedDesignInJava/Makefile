TEXPROCESSOR := pdflatex
TEXFLAGS := -shell-escape

TARGET := oodesign_java_notes
SOURCES := $(wildcard *.tex)


all: $(TARGET).pdf clean

debug: $(TARGET).pdf


$(TARGET).pdf: $(SOURCES)
	$(TEXPROCESSOR) $(TEXFLAGS) main.tex &&\
		mv main.pdf $(TARGET).pdf


read: $(TARGET).pdf
	evince $(TARGET).pdf &


clean:
	-rm *.log 
	-rm *.aux
	-rm *.out 
	-rm *.dvi 
	-rm *.bbl 
	-rm *.blg
	-rm -r _minted*

cleanall: clean
	-rm *.pdf


.PHONY: all read clean cleanall
