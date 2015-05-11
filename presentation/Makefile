LFLAGS = -pdf

all: graph1 master
clean: cleanmaster cleangraph1

master: setupmaster
	cd dest && latexmk $(LFLAGS) presentation.tex
	cd dest && cp presentation.pdf ..

setupmaster:
	mkdir -p dest
	cp -r *.tex imgs dest

cleanmaster:
	rm -rf dest
	rm -f presentation.pdf

graph1: setupgraph1
	cd graph1/dest && pdflatex -shell-escape graph1.tex
	cd graph1/dest && convert -density 500 -resize 1920x1080 graph1.svg graph1.png
	cd graph1/dest && cp graph1.png ../../imgs/graph1.png

setupgraph1:
	cd graph1 && mkdir -p dest
	cd graph1 && cp *.tex dest

cleangraph1:
	cd graph1 && rm -rf dest
	cd imgs && rm -rf graph1.png
