# govstyle

A package for producing graphics following the [gov.uk](http://www.gov.uk) style.

## Functions

* `theme_gov()`: Theme to be applied to plots produced in [ggplot2]() to give a government statistics publication feel.

## Colour lists

* `gov_cols`: A vector of the [gov.uk]() approved colours.

## Examples




```r
library(ggplot2)
library(dplyr)
#devtools::install_github("ivyleavedtoadflax/govstyle")
library(govstyle)
```


```r
p <- mtcars %>%
  ggplot +
  aes(
    x = wt,
    y = mpg,
    col = factor(cyl)
    ) +
  geom_point()

p
```

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3-1.png)

```r
p +
  theme_gov()
```

![plot of chunk unnamed-chunk-3](figure/unnamed-chunk-3-2.png)
