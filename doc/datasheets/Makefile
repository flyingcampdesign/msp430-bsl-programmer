
SUBDIRS=fcd-prg01
PDFLATEX="TEXINPUTS=\".:..:\" pdflatex"

all:
	for D in $(SUBDIRS); do make -C $$D; done

clean:
	rm -f *~
	for D in $(SUBDIRS); do make -C $$D clean; done
