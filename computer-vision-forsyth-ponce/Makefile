SRCS = $(wildcard *.md)
PDFS = $(subst .md,.pdf,$(SRCS))

all: *.md
	pandoc $(SRCS) -o $(PDFS)

clean: *.pdf
	rm -f *.pdf