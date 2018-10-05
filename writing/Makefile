all: change nochange clean

change:	mol_epi_2D.tex ref.bib
	latexdiff --graphics-markup=0 --disable-citation-markup old.tex mol_epi_2D.tex > change.tex
	latexmk -pdf -f -quiet -pdflatex="xelatex -interaction=nonstopmode --shell-escape" change.tex

nochange: mol_epi_2D.tex ref.bib
	latexmk -pdf -f -quiet -pdflatex="xelatex -interaction=nonstopmode --shell-escape" mol_epi_2D.tex

clean:
	latexmk -c

cleanall:
	latexmk -C
