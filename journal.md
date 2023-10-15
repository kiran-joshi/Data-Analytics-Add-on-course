---
title: A Bussiness model proposal based on customer feedback
author:
  - name: KiranJoshi
    email: kiran@vjecin
    affiliation: Vimal Jyothi Engineering College
    correspondingauthor: true
    footnote: 1
  - name: Faiza Fathima
    email: faizanadeer@vjec.in
    affiliation: Vimal Jyothi Engineering College
  - name: Adwaith Raj
    email: adwaith@vjec.in
    affiliation: Vimal Jyothi Engineering College
    footnote: 2
  - name: Nihara Rajith
    email: nihara@vjec.in
    affiliation: Vimal Jyothi Engineering College
    footnote: 2
address:
  - code: Vimal Jyothi Engineering College
    organization: KTU
    addressline: Chemperi
    city: Kannur
    state: Kerala
    postcode: 670632
    country: India
  - code: 
    organization: Department Of Computer Science And Bussiness Systems
    addressline: 
    postcode: 
    city: 
    country: 
footnote:
  - code: 1
    text: "This is the first author footnote."
  - code: 2
    text: "Another author footnote."
abstract: This article is a short analysis of the data collected from the course participants of the `Fundamentals of Data Analytics using R Programming`. A baseline descriptive analysis is conducted and the results are tested using hypothesis testing for generalizations.
  
keywords: 
  - keyword1
  - keyword2
journal: "Journal Of Compuetr Science And Bussiness Systems"
date: "`r Sys.Date()`"
classoption: preprint, 3p, authoryear
bibliography: mybibfile.bib
linenumbers: false
numbersections: true
# Use a CSL with `citation_package = "default"`
# csl: https://www.zotero.org/styles/elsevier-harvard
output: 
  rticles::elsevier_article:
    keep_tex: true
    citation_package: natbib
---

Please make sure that your manuscript follows the guidelines in the 
Guide for Authors of the relevant journal. It is not necessary to 
typeset your manuscript in exactly the same way as an article, 
unless you are submitting to a camera-ready copy (CRC) journal.

For detailed instructions regarding the elsevier article class, see   <https://www.elsevier.com/authors/policies-and-guidelines/latex-instructions>

# Bibliography styles

Here are two sample references: @Feynman1963118 [@Dirac1953888].

By default, natbib will be used with the `authoryear` style, set in `classoption` variable in YAML. 
You can sets extra options with `natbiboptions` variable in YAML header. Example 
```yaml
natbiboptions: longnamesfirst,angle,semicolon
```

There are various more specific bibliography styles available at
<https://support.stmdocs.in/wiki/index.php?title=Model-wise_bibliographic_style_files>. 
To use one of these, add it in the header using, for example, `biblio-style: model1-num-names`.

## Using CSL 

If `citation_package` is set to `default` in `elsevier_article()`, then pandoc is used for citations instead of `natbib`. In this case, the `csl` option is used to format the references. Alternative `csl` files are available from <https://www.zotero.org/styles?q=elsevier>. These can be downloaded
and stored locally, or the url can be used as in the example header.

# Equations

Here is an equation:
$$ 
  f_{X}(x) = \left(\frac{\alpha}{\beta}\right)
  \left(\frac{x}{\beta}\right)^{\alpha-1}
  e^{-\left(\frac{x}{\beta}\right)^{\alpha}}; 
  \alpha,\beta,x > 0 .
$$

Here is another:
\begin{align}
  a^2+b^2=c^2.
\end{align}

Inline equations: $\sum_{i = 2}^\infty\{\alpha_i^\beta\}$

# Figures and tables

Figure \ref{fig2} is generated using an R chunk.

```{r fig2, fig.width = 5, fig.height = 5, fig.align='center', out.width="50%", fig.cap = "\\label{fig2}A meaningless scatterplot.", echo = FALSE}
plot(runif(25), runif(25))
```

# Tables coming from R

Tables can also be generated using R chunks, as shown in Table \ref{tab1} for example.

```{r tab1, echo = TRUE}
knitr::kable(head(mtcars)[,1:4], 
    caption = "\\label{tab1}Caption centered above table"
)
```

# References {-}

