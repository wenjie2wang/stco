render2pdf:
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');" \
	-e "f <- list.files(pattern = '*\\\.Rmd', )" \
	-e "rmarkdown::render(f[1], 'pdf_document')"

render2md:
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');" \
	-e "f <- list.files(pattern = '*\\\.Rmd', )" \
	-e "rmarkdown::render(f[1], 'md_document')"

clean: 
	rm -rf *_files *_cache .Rhistory *\#* .\#* *.tar.gz *~
