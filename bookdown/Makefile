sourceRmd := $(wildcard *.Rmd)
yaml := $(wildcard *.yml)
outName := $(shell grep "book_filename:" _bookdown.yml\
	| sed "s/book_filename: //" | sed 's/"//g')
pdf := _book/$(outName).pdf
gitbook := _book/$(outName).html


.PHONY: all
all: $(pdf) # $(gitbook)

$(pdf): $(sourceRmd) $(yaml)
	Rscript -e "bookdown::render_book('.')"

$(gitbook): $(sourceRmd) $(yaml)
	Rscript -e "bookdown::render_book('.', 'bookdown::gitbook')"


.PHONY: clean
clean:
	rm -rf *_files *_cache .Rhistory *\#* .\#* *.tar.gz *~
