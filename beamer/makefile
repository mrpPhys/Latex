#-------------------------------------------------------------------------------
# @author: Miguel Ramos Pernas
# @email:  miguel.ramos.pernas@gmail.com
#-------------------------------------------------------------------------------
#
# Description:
#
# Makefile to compile latex code. The output file must be defined in
# < OUTPUTFILE >, while the main file is specified in < MAIN >.
#
#-------------------------------------------------------------------------------

# Output and main files, and command to compile the code
OUTPUTFILE = MyOutputFile
MAIN       = template
CMD        = pdflatex

FIGURES=$(wildcard ./figs/*)
SOURCE=$(wildcard *.tex) $(wildcard *.sty) $(wildcard *.bib)
OUTPUT=$(OUTPUTFILE).pdf

$(OUTPUT): $(MAIN).tex $(SOURCE) $(FIGURES) makefile
	$(CMD) $<
ifneq ($(OUTPUT),$(MAIN).pdf)
	@mv $(MAIN).pdf $(OUTPUT)
	@echo Output file renamed as $(OUTPUT)
endif
clean:
	rm -f *~ *.aux *.snm *.nav *.toc *.log *.bbl *.blg *.dvi *.tmp *.out *.blg *.bbl $(OUTPUT)
