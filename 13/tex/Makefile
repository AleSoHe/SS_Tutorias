filename=main

.PHONY:

pdf:
	pdflatex --shell-escape $(filename).tex
	pdflatex --shell-escape $(filename).tex
	okular main.pdf

images:
	cd figs; echo "I'm in some_dir"; \
	pdflatex --shell-escape time1.tex; \
	pdflatex --shell-escape time2.tex; \
	pdflatex --shell-escape time3.tex; \
	pdflatex --shell-escape time4.tex; \
	pdflatex --shell-escape re1.tex; \
	pdflatex --shell-escape re2.tex; \
	pdflatex --shell-escape re3.tex; \
	pdflatex --shell-escape re4.tex; \
	pdflatex --shell-escape im1.tex; \
	pdflatex --shell-escape im2.tex; \
	pdflatex --shell-escape im3.tex; \
	pdflatex --shell-escape im4.tex; \
	cd .. \

read:
	evince ${filename}.pdf &

clean:
	rm -f ${filename}.{ps,pdf,log,aux,out,dvi,bbl,blg,html}
	latexmk -c
