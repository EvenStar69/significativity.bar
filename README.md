# Significativity Bar

R package for drawing significativity bars in ggplot. 

Works for dotplots and barplots.

For more details on the function, feel free to use the R manual with the command `?significativity_bar` once the package is installed.

# Installation

This code installs the significativity.bar package from this depository :

```r
install.packages("devtools")
library(devtools)

install_github("EvenStar69/significativity.bar/significativity.bar")
library(significativity.bar)
```

# Example

This code provide an example of utilisation of the package to draw a significativity bar in a dotplot :

```r
install.packages("ggplot2")
library(ggplot2)

my_ggplot <- ggplot(data = ToothGrowth[,-2], aes(x = dose, y = len)) + geom_point(color = "lightblue")
my_ggplot

my_ggplot_with_bar <- significativity_bar(plot = my_ggplot, groups = c(1,2), text = "**")
```
