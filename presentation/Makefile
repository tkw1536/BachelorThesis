LFLAGS = -pdf

all: clean setup
	cd dest && latexmk $(LFLAGS) presentation.tex
	cd dest && cp presentation.pdf ..

setup:
	mkdir dest
	cp -r *.tex imgs dest

clean:
	rm -rf dest
	rm -f presentation.pdf
