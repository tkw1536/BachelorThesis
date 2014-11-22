LFLAGS = -pdf

all: clean setup
	cd dest && latexmk $(LFLAGS) proposal.tex
	cd dest && cp proposal.pdf ..

setup:
	mkdir dest
	cp -r *.tex *.bib img dest

clean:
	rm -rf dest
	rm -f proposal.pdf
