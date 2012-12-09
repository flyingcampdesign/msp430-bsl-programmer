PROJ=10001_msp430_bsl_programmer
REV=1.1.1

eagle:
	zip -r	${PROJ}_${REV}.zip \
		${PROJ}.sch \
		${PROJ}.brd \
		${PROJ}_bom.xls \
		Makefile \
		README_PCB.txt \
		LICENSE.txt \

fab:
	zip	${PROJ}_${REV}_fab.zip \
		*.art \
		${PROJ}.mnt \
		${PROJ}.mnb \
		${PROJ}_bom.xls \
		NCDRILL.txt \
		${PROJ}_photoplots.pdf \
		README_PCB.txt \
		LICENSE.txt \

all: eagle fab

tidy:
	rm -vf	*~ \
		*.*#* \
		Transcode\ Report.txt \

tidyart:
	rm -vf	*.gpi \
		*.dri \

tidyall: tidy tidyart

cleanart:
	rm -vf	*.art \
		*.gpi \
		${PROJ}_photoplots.pdf \
		NCDRILL.* \

cleanplace:
	rm -vf	*.mnt \
		*.mnb \

cleanzip:
	rm -vf	${PROJ}_${REV}_fab.zip \
		${PROJ}_${REV}.zip \

cleandirs:
	rm -rvf	${PROJ}_${REV}_fab \
		${PROJ}_${REV} \

cleanup: tidyall cleandirs

clean: tidyall cleanart cleanplace cleanzip cleandirs
