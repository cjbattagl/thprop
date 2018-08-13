.DEFAULT_GOAL := all

DRAFT_BUILD_DIR = draft

thprop: draft-build-dir $(DRAFT_BUILD_DIR)/thprop.pdf

#all: draft-build-dir sisc sc ics
all: draft-build-dir thprop

.PHONY: draft-build-dir
draft-build-dir:
	test -d $(DRAFT_BUILD_DIR)/ || mkdir -p $(DRAFT_BUILD_DIR)

.PHONY: $(DRAFT_BUILD_DIR)/thprop.pdf
$(DRAFT_BUILD_DIR)/thprop.pdf:
	latexmk -f -pdf -output-directory=$(DRAFT_BUILD_DIR)/ thprop.tex
clean:
	rm -rf $(DRAFT_BUILD_DIR)/ *~ core *.blg *.toc *.bbl *.out *.aux *.log

# eof
