ALL=man1/pandoc-citeproc.1
DATE=$(shell date "+%Y-%m-%d")
VERSION=$(shell ../dist/build/pandoc-citeproc/pandoc-citeproc --version | head -1 | awk '{print $$2;}')

.PHONY: all

all: $(ALL)
man1/%.1: %.1.md ../dist/build/pandoc-citeproc/pandoc-citeproc
	pandoc $< -o $@ -s -t man -Vfooter="${VERSION}" -Vdate="${DATE}"
