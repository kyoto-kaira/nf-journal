compile:
	uplatex nf2025.tex
	upbibtex nf2025
	uplatex nf2025.tex
	uplatex nf2025.tex
	dvipdfmx nf2025.dvi

clean:
	rm -f *.aux *.log *.dvi *.toc *.out *.bbl *.blg *.fls *.fdb_latexmk *.synctex.gz

.PHONY: compile clean
