

# tcctemplate 0.1.0

<!-- [![Build Status](https://travis-ci.org/leg-ufpr/legtheme.svg?branch=master)](https://travis-ci.org/leg-ufpr/legtheme) -->

DEST UFPR template for documents.

## Usage

<!-- After installing (sse below), you can create a draft document from one -->
<!-- of the themes available: -->

<!-- - `beamer_leg` is a theme for beamer slides -->
<!-- - `proj_generico` is a theme for a generic project or any other similar -->
<!--   document in PDF -->

### In RStudio

1. In the menu go to `File > New File > R Markdown...`
2. In the opening window, choose `From Template`, then select
`DEST UFPR Project Template {tcctemplate}`
3. Give a name and choose a location then clicl `Ok`

### Outside RStudio

To create a draft use:


```r
library(rmarkdown)
draft(file = "Projeto.Rmd", template = "projeto-template",
      package = "tcctemplate", create_dir = TRUE, edit = FALSE)
```
This will create a directory named `Projeto` with all files needed. Open
`Projeto.Rmd` and render it with


```r
render("Projeto.Rmd")
```

<!-- Similarly, to create a draft document for the `proj_generico` theme, -->
<!-- just use: -->



## Download and install

The easiest way to install is directly from this repository with the
**remotes** (or **devtools**) packages


```r
## install.packages("remotes")
remotes::install_github("fernandomayer/tcctemplate")
```

## Authors

- [Fernando de Pol Mayer][]

## License

MIT. See [LICENSE](./LICENSE)

<!-- links -->


[Fernando de Pol Mayer]: http://www.leg.ufpr.br/~fernandomayer
