PROJ=10002_msp430_bsl_programmer_cable
REV=1.1

eagle:
	zip -r	${PROJ}_${REV}.zip \
		${PROJ}.sch \
		${PROJ}_bom.xls \
		Makefile \
		LICENSE.txt \

mfr:
	zip -r	${PROJ}_${REV}_mfr.zip \
		${PROJ}_bom.xls \
		${PROJ}_schematic.pdf \
		LICENSE.txt \

all: eagle mfr

tidy:
	rm -vf	*~ \
		*.*#* \

cleanart:
	rm -vf	${PROJ}_schematic.pdf \

cleanzip:
	rm -vf	${PROJ}_${REV}_mfr.zip \
		${PROJ}_${REV}.zip \

cleandirs:
	rm -rvf	${PROJ}_${REV}_mfr \
		${PROJ}_${REV} \

cleanup: tidy cleandirs

clean: tidy cleanart cleanzip cleandirs
