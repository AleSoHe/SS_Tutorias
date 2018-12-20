filename=main

.PHONY:

pdf:
	pdflatex $(filename).tex
	pdflatex $(filename).tex
	okular main.pdf

images:
	pdflatex --output-directory ./figs/ ./figs/diracs_train.tex
	okular figs/diracs_train.pdf

read:
	evince ${filename}.pdf &

clean:
	rm -f ${filename}.{ps,pdf,log,aux,out,dvi,bbl,blg,html}
	latexmk -c
