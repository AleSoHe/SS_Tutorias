filename=main

.PHONY:

pdf:
	pdflatex $(filename).tex
	pdflatex $(filename).tex
	okular main.pdf

text: html
	html2text -width 100 -style pretty ${filename}/${filename}.html | sed -n '/./,$$p' | head -n-2 >${filename}.txt

html:
	@#latex2html -split +0 -info "" -no_navigation ${filename}
	htlatex ${filename}

read:
	evince ${filename}.pdf &

clean:
	rm -f ${filename}.{ps,pdf,log,aux,out,dvi,bbl,blg,html}
	latexmk -c
