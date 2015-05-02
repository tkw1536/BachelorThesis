LFLAGS = -pdf

all: clean setup
	cd dest && latexmk $(LFLAGS) thesis.tex
	cd dest && cp thesis.pdf ..

setup:
	mkdir dest
	cp -r *.tex *.bib parts img dest

clean:
	rm -rf dest
	rm -f thesis.pdf
