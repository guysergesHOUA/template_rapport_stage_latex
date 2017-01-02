FILE := rapport_stage_octo_agiraldo_V1_S1_07_2017

.PHONY: clean all read dev

all: dev clean

dev:
	latexmk -pdf $(FILE)
	$(MAKE) read

read:
	open $(FILE).pdf &

clean:
	latexmk -c
	rm -f *.glo *.ist *.ascript *.apc *.bbl *.bib *.xml *.glsdefs *.acn
