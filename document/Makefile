
# MAIN LATEXMK RULE

# -pdf tells latexmk to generate PDF directly (instead of DVI).
# -pdflatex="" tells latexmk to call a specific backend with specific options.
# -use-make tells latexmk to call make for generating missing files.

# -interaction=nonstopmode keeps the pdflatex backend from stopping at a
# missing file reference and interactively asking you for an alternative.

default: master.tex
#	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -use-make master.tex
	latexmk -pdf -pdflatex="pdflatex" -use-make master.tex
watch: master.tex
	latexmk -pdf -pdflatex="pdflatex -interaction=nonstopmode" -pvc -use-make master.tex
#	latexmk -pdf -pdflatex="pdflatex" -pvc -use-make master.tex
clean:
	latexmk -CA
	rm general.bib
