render2pdf:
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');" \
	-e "f <- list.files(pattern = '*\\\.Rmd', )" \
	-e "rmarkdown::render(f[1], 'pdf_document')"

render2html:
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');" \
	-e "f <- list.files(pattern = '*\\\.Rmd', )" \
	-e "rmarkdown::render(f[1], 'html_document')"

clean: 
	rm -rf *_files *_cache .Rhistory *\#* .\#* *.tar.gz *~
