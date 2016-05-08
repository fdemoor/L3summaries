################################################################################
##################### GENERIC MAKEFILE FOR PDF REPORTS #########################
################################################################################

tex=$(wildcard *.tex)
pdf=$(tex:.tex=.pdf)
vw=$(tex:.tex=.vw) # HACK to allow multiple pdf's being opened at once

all: $(pdf)

%.pdf: %.tex
	pdflatex $< && pdflatex $<

clean: 
	rm -f $(pdf) *.aux *.log

%.vw: %.pdf
	xdg-open $(<:.vw=.pdf) &>/dev/null &

view: $(vw)
