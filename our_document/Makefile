
DOC = report
COVER = frontpage/frontpage

all: $(DOC)

frontpage: frontpage/frontpage.tex
	make -C frontpage all

$(DOC): $(DOC).pdf openpdf

openpdf:
	open $(DOC).pdf

%.pdf: %.tex
	pdflatex $(DOC) && makeglossaries $(DOC) && pdflatex $(DOC) && bibtex $(DOC) && pdflatex $(DOC) && pdflatex $(DOC)
	# pdflatex $(DOC)

clean:
	rm -rf $(DOC).aux $(DOC).bbl $(DOC).log $(DOC).lot $(DOC).blg $(DOC).lol \
	$(DOC).toc $(DOC).out $(DOC).glg $(DOC).glo $(DOC).gls $(DOC).ist \
	$(DOC).lof $(DOC).pdf
