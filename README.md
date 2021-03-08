

# legtheme 0.0.1

[![Build Status](https://travis-ci.org/leg-ufpr/legtheme.svg?branch=master)](https://travis-ci.org/leg-ufpr/legtheme)

LEG template for documents.

## Usage

After installing (sse below), you can create a draft document from one
of the themes available:

- `beamer_leg` is a theme for beamer slides
- `proj_generico` is a theme for a generic project or any other similar
  document in PDF

To create a draft for `beamer_leg` use:


```r
library(rmarkdown)
draft(file = "slides.Rmd", template = "beamer_leg",
      package = "legtheme", create_dir = FALSE, edit = FALSE)
```
This will create (in the current directory) a file named `slides.Rmd`
which can be further rendered with


```r
render("slides.Rmd")
```

Similarly, to create a draft document for the `proj_generico` theme,
just use:


```r
draft(file = "proj.Rmd", template = "proj_generico",
      package = "legtheme", create_dir = FALSE, edit = FALSE)
render("proj.Rmd")
```

## Download and install

The easiest way to install is directly from this repository with the
**remotes** (or **devtools**) packages


```r
remotes::install_github("leg-ufpr/legtheme")
```

In any case, there are detailed instructions below for different
plataforms.

### Linux/Mac

Use the `remotes` package (available from
[CRAN](http://cran-r.c3sl.ufpr.br/web/packages/remotes/index.html)) to
install automatically from this GitHub repository:


```r
library(remotes)
install_github("leg-ufpr/legtheme")
```

Alternatively, download the package tarball: [legtheme_0.0.1.tar.gz][]
and run from a UNIX terminal (make sure you are on the container file
directory):


```
R CMD INSTALL -l /path/to/your/R/library legtheme_0.0.1.tar.gz
```

Or, inside an `R` session:


```
install.packages("legtheme_0.0.1.tar.gz", repos = NULL,
                 lib.loc = "/path/to/your/R/library",
                 dependencies = TRUE)
```

Note that `-l /path/to/your/R/library` in the former and `lib.loc =
"/path/to/your/R/library"` in the latter are optional. Only use it if
you want to install in a personal library, other than the standard R
library.

### Windows

Download Windows binary version: [legtheme_0.0.1.zip][] (**do not unzip
it under Windows**), put the file in your working directory, and from
inside `R`:


```
install.packages("legtheme_0.0.1.zip", repos = NULL,
                 dependencies = TRUE)
```

## Authors

- Original [theme](https://github.com/coatless/uiucthemes)
  (`uiucthemes`) by [James L. Balamuta](https://github.com/coatless)
- LEG theme adaptation by:
  - [Fernando de Pol Mayer][]

## Documentation

The reference manual in PDF can be found here: [legtheme-manual.pdf][]

## License

MIT. See [LICENSE](./LICENSE)

<!-- links -->



[legtheme_0.0.1.tar.gz]: https://github.com/leg-ufpr/legtheme/raw/master/downloads/legtheme_0.0.1.tar.gz
[legtheme_0.0.1.zip]: https://github.com/leg-ufpr/legtheme/raw/master/downloads/legtheme_0.0.1.zip
[legtheme-manual.pdf]: https://github.com/leg-ufpr/legtheme/raw/master/downloads/legtheme-manual.pdf
[Fernando de Pol Mayer]: http://www.leg.ufpr.br/~fernandomayer
