##################################################################
# Makefile for LaTeX
##################################################################
# Use:
# make
# make clean
# options for ps2pdf: http://pages.cs.wisc.edu/~ghost/doc/AFPL/6.50/Ps2pdf.htm

TEX:=$(shell ls *.tex)
OTHER = *~ *.aux *.dvi *.toc *.bbl *.blg *.gz *.out *.thm *.ps *.idx *.ilg *.ind

pdflatex: master.tex
	pdflatex --synctex=1 master.tex
	bibtex master.aux
	pdflatex --synctex=1 master.tex
	echo "----last-run----"
	pdflatex --synctex=1 master.tex
	rm -f $(OTHER) $(PS)
watch: master.tex
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -pvc -use-make master.tex
#	latexmk -pdf -pdflatex="pdflatex" -pvc -use-make master.tex
clean:
	rm -f $(OTHER) $(PS)
