TEX = pdflatex -shell-escape

.PHONY: all view

all : pdf
	make view

view :
	okular main.pdf

pdf : main.tex
	$(TEX) main.tex

clean:  
	find . -type f | xargs touch
	rm -rf $(OBJS)
