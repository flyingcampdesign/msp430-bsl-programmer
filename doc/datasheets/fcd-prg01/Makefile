
include ../Makefile.inc

msp430-prog.pdf: fcd-prg01.tex ../datasheet.cls
	$(PDFLATEX) $<
	$(PDFLATEX) $<
	$(PDFLATEX) $<

clean:
	rm -rf *.pdf *~ *.log *.dvi *.out *.aux *.synctex.gz
