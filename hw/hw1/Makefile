render2pdf:
	Rscript -e "if(! require(rmarkdown)) install.packages('rmarkdown');" \
	-e "f <- list.files(pattern = 'hw[0-9]\\\.Rmd', )" \
	-e "rmarkdown::render(f[1], 'pdf_document')"

render2html:
	sed "s/\\\bm//g" $${PWD##*/}.Rmd >hwHtml.Rmd;\
	Rscript -e "rmarkdown::render('hwHtml.Rmd', 'html_document')" ;\
	rm hwHtml.Rmd;\
	mv hwHtml.html $${PWD##*/}.html

clean:
	rm -rf *_files *_cache .Rhistory *\#* .\#* *.tar.gz *~
