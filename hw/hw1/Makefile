render:
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');" \
	-e "f <- list.files(pattern = '*\\\.Rmd', )" \
	-e "rmarkdown::render(f[1])"

clean: 
	rm -rf *_files *_cache .Rhistory *\#* *.tar.gz *~
