## Paquete tosr 

# Paso 1
Primero se debe instalar el paquete "remote" que sirve para gestionar el paquete 'tosr' en el Rstudio cloud. La siguiente instruccion se copia y se pega en la consala y se ejecuta. 

install.packages("remotes")

# Paso 2
Para instalar el paquete de tosr en el Rstudio cloud se copia la siguiente instruccion y se ejecuta. Se espera un momento a que instale y luego se puede usar el paquete.  

remotes::install_github("https://github.com/coreofscience/tosr" , dependencies = TRUE)

# Ejemplo
1. library(tosr)
2. tosinfo <- tosr('scopus.bib')

3. tos.df      <- tosinfo$bibliometrix_df
4. tos.g       <- tosinfo$graph
5. tos.tos_sub <- tosinfo$ToS_subfields
6. tos.cited   <- tosinfo$cited_references

# **Analisis bibliometrico**
tosr_bibliometix_analysis(tos.df)

# **Wordcloud**
1. tosr_wordcloud(tos.cited, tos.tos_sub, subfield = 1) 
2. tosr_wordcloud(tos.cited, tos.tos_sub, subfield = 2)
3. tosr_wordcloud(tos.cited, tos.tos_sub, subfield = 3)

# Referencias
1. https://revistas.unal.edu.co/index.php/ingeinv/article/view/77718/0
2. https://rdrr.io/cran/remotes/man/install_git.html
2. https://www.bibliometrix.org/
