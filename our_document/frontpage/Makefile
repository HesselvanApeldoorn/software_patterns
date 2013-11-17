
COVER = frontpage

all: $(COVER)

$(COVER): $(COVER).pdf

%.pdf: %.tex
	pdflatex $(COVER)

clean:
	rm -rf $(COVER).aux $(COVER).log
