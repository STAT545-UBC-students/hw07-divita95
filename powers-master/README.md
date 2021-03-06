
<!-- README.md is generated from README.Rmd. Please edit that file -->

[![Build
Status](https://travis-ci.org/vincenzocoia/powers.svg?branch=master)](https://travis-ci.org/vincenzocoia/powers)

# STAT547-Homework Assignment#7

This assignment was made by **Divita Pal**. An R package `powers` was developed with the help of `devtools` and `testthat` packages. This involves adding functionality to the `powers` package and then testing the correctness of the functions developed using 'testthat` package.

# powers

This is an R package that gives `sqrt()`, `cube()`, `reciprocal()` and also shows the use of family of `BoxCox transformation functions` 

## Installation

You can install powers from github with:

``` r
# install.packages("devtools")
devtools::install_github("STAT545-UBC-students/hw07-divita95/tree/master/powers-master", build_vignettes = T)
```

## Workflow

The R package was using the two packages mentioned above. Links to relevant folders are as follows:
1. [R](https://github.com/STAT545-UBC-students/hw07-divita95/tree/master/powers-master/R) : Gives the functions that are included in the package
2. [tests](https://github.com/STAT545-UBC-students/hw07-divita95/tree/master/powers-master/tests) : Shows the tests that were performed to validate the functions
3. [README](https://github.com/STAT545-UBC-students/hw07-divita95/blob/master/powers-master/README.md) : Gives details about despriction, installation and workflow
4. [Vignette](https://github.com/STAT545-UBC-students/hw07-divita95/tree/master/powers-master/vignettes) : Gives the examples for better understanding


## Example

See the vignette for more extensive use, but here’s an example:

``` r
powers::reciprocal(2)
#> [1] 0.5
powers::square(3)
#> [1] 9
powers::boxcox(0,1)
#> [1] -1
```

## For Developers

(Again, I don’t actually intend for anyone to develop this silly
package, but if I did, here’s what I’d write.)

Use the internal `pow` function as the machinery for the front-end
functions such as `square`, `cube`, and `reciprocal`.
