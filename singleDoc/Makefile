sourceDoc := $(wildcard *.Rmd)
pdf := $(patsubst %.Rmd,%.pdf,$(sourceDoc))
html := $(patsubst %.Rmd,%.html,$(sourceDoc))

.PHONY: all
all: $(pdf) $(html)

%.pdf: %.Rmd
	@echo -e "\ncompiling $? to pdf..."
	Rscript -e "rmarkdown::render('$?', bookdown::pdf_document2(toc = FALSE))"

%.html: %.Rmd
	@echo -e "\ncompiling $? to html..."
	Rscript -e "rmarkdown::render('$?', bookdown::html_document2(toc = FALSE))"


.PHONY: clean
clean:
	rm -rf *_files *_cache .Rhistory *\#* .\#* *.tar.gz *~
