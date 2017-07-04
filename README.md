# currency — Formatting currencies


## Overview

`currency` is a LaTeX package that facilitates the formatting
of currencies (amounts and units). It is based on the `siunitx` package
for printing numbers.

For instance, this code in the preamble defines a EUR monetary unit 

``` latex
\DefineCurrency{EUR}{name={euro},plural={euros},symbol={\euro},iso={EUR},kind=iso,base=2}
```

that will be used later by 

``` latex
\dEUR{123} or \dEUR[kind=plural]{123}
```
to print `123 EUR or 123 euros`. There are many ways to change to output 
(the symbol could be put in front of the amount as required by some 
typographical conventions, ...).


See the [documentation](https://github.com/antoinelejay/currency/blob/master/currency_doc.pdf)
for examples and installation instructions.

## License

This work may be distributed and/or modified under the conditions of the
[LaTeX Project Public License](http://www.latex-project.org/lppl.txt) (LPPL),
version 1.3 or later.

Please use the project's GitHub site at <https://github.com/antoinelejay/currency>
for suggestions, feature requests, and bug reports.

## Installation

```
pdflatex currency.ins
pdflatex currency.dtx
makeindex -s gind.ist currency.idx
makeindex -s gglo.ist -o currency.gls currency.glo
pdflatex currency.dtx

pdflatex currency_doc.tex
biber currency_doc
pdflatex currency_doc.tex
```

## Availability

This package is available on [github](https://github.com/antoinelejay/currency) and on 
[CTAN](http://www.ctan.org/tex-archive/macros/latex/contrib/currency)

