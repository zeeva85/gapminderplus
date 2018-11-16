
<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Build Status](https://travis-ci.org/vincenzocoia/powers.svg?branch=master)](https://travis-ci.org/vincenzocoia/powers)

**Note**: This R package is not mean to be "serious". It's just to show you are kinda cool and you can develop simple packages :sunglasses:.

gapminderplus
=============

This is an R package that has extended the gapminder dataset. This package also has included a simple `subset_country()` function which returns the mini dataset that was required for as many countries possible.

Installation
------------

You can install powers from github with:

``` r
# install.packages("devtools")
devtools::install_github("STAT545-UBC-students/hw07-zeeva85/gapminderplus")
```

Example
-------

``` r
library(gapminderplus)


head(gapminder2)
       country continent year lifeExp      pop gdpPercap meanSchool
 1 Afghanistan      Asia 1972  36.088 13079460  739.9811        1.1
 2 Afghanistan      Asia 1977  38.438 14880372  786.1134        1.4
 3 Afghanistan      Asia 1982  39.854 12881816  978.0114        1.8
 4 Afghanistan      Asia 1987  40.822 13867957  852.3959        2.1
 5 Afghanistan      Asia 1992  41.674 16317921  649.3414        2.3
 6 Afghanistan      Asia 1997  41.763 22227415  635.3414        2.6

tail(gapminder3)
     country continent year lifeExp      pop gdpPercap meanSchool infantMortality
519   Zambia    Africa 2002  39.193 10595811 1071.6139        7.9            86.5
520   Zambia    Africa 2007  42.384 11746035 1271.2116        8.0            61.3
521 Zimbabwe    Africa 1992  60.377 10704340  693.4208        8.4            54.5
522 Zimbabwe    Africa 1997  46.809 11404948  792.4500        9.0            62.7
523 Zimbabwe    Africa 2002  39.989 11926563  672.0386        9.6            62.7
524 Zimbabwe    Africa 2007  43.487 12311143  469.7093       10.0            59.9

......

subset_country2() # Notice country format, Caps followed by lowercase, empty value ends prompt
#> [1] country         continent       year            lifeExp        
#> [5] pop             gdpPercap       meanSchool      infantMortality
#> <0 rows> (or 0-length row.names)

subset_country() # Notice country format, Caps followed by lowercase, empty value ends prompt
#> [1] country    continent  year       lifeExp    pop        gdpPercap 
#> [7] meanSchool
#> <0 rows> (or 0-length row.names)
```

Console view
------------
```
# 1: Japan
# 2:              # Notice country format, Caps followed by lowercase, empty value ends prompt
# Read 1 item 
```
```
  country continent year lifeExp       pop gdpPercap meanSchool
1   Japan      Asia 1972  73.420 107188273  14778.79       10.4
2   Japan      Asia 1977  75.380 113872473  16610.38       11.0
3   Japan      Asia 1982  77.110 118454974  19384.11       11.5
4   Japan      Asia 1987  78.670 122091325  22375.94       12.0
5   Japan      Asia 1992  79.360 124329269  26824.90       12.5
6   Japan      Asia 1997  80.690 125956499  28816.58       12.9
7   Japan      Asia 2002  82.000 127065841  28604.59       13.2
8   Japan      Asia 2007  82.603 127467972  31656.07       13.5
```


For Developers
--------------

(Again, I don't actually intend for anyone to develop this silly and cool package, but if I did, here's what I'd write.)

Develop the subset function to accept values within its function and console. Add additional dataset available in the `data-raw` folder to the `gapminder2` dataset.
