sourceDoc := $(wildcard *.Rmd)
pdf := $(patsubst %.Rmd,%.pdf,$(sourceDoc))
html := $(patsubst %.Rmd,%.html,$(sourceDoc))

.PHONY: all
all: $(pdf) $(html)

%.pdf: %.Rmd
	@echo "compiling $? to pdf..."
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');"\
		-e "rmarkdown::render('$?', 'pdf_document')"
	@echo "$@ is generated.\n"

%.html: %.Rmd
	@echo "compiling $? to html..."
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');"\
		-e "rmarkdown::render('$?', 'html_document')"
	@echo "$@ is generated.\n"


.PHONY: clean
clean:
	rm -rf *_files *_cache .Rhistory *\#* .\#* *.tar.gz *~
