#
# Makefile zum Skript ueber High Performance Computing
#
# (c) 2013 Prof Dr Andreas Mueller, Hochschule Rapperswil
#
SAMPLEFILES = sample/sample.tex sample/sample.bib

TEXFILES = vorwort.tex einleitung.tex maschinen.tex sprachen.tex \
	daten.tex algorithm.tex $(SAMPLEFILES)

BLXFILES = skript1-blx.bbl skript2-blx.bbl

skript.pdf:	skript.tex $(TEXFILES) skript.ind $(BLXFILES)
	pdflatex skript.tex
	bibtex skript

skript.ind:	skript.tex $(TEXFILES)
	touch skript.ind
	pdflatex skript.tex
	makeindex skript.idx

# References

skript.bbl:		skript.aux
	bibtex skript

skript1-blx.bbl:	skript1-blx.aux
	bibtex skript1-blx

skript2-blx.bbl:	skript2-blx.aux
	bibtex skript2-blx
