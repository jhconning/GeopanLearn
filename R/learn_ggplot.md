---
title: "R for Data Science"
output: 
  html_document: 
    keep_md: yes
---

This is a [R Markdown](http://rmarkdown.rstudio.com) Notebook.  Pressing *Ctrl+Shift+Enter* runs the chunk. 


```r
library(gapminder)
library(dplyr)
library(ggplot2)
```

*Insert Chunk* on the toolbar or by pressing *Ctrl+Alt+I*.

When you save the notebook, an HTML file containing the code and output will be saved alongside it (click the *Preview* button or press *Ctrl+Shift+K* to preview the HTML file). The keep_md; true flag makes sure we also keep an intermediate markdown file with output which can be displayed on github.

Unlike *Knit*, *Preview* does not run any R code chunks, what was last run in the editor is displayed.


```r
gapminder_1952 = gapminder %>% filter(year==1952)
ggplot(gapminder_1952, aes(x=gdpPercap, y = lifeExp, size= pop, color=continent)) +
   geom_point() +xlim(0,15000)
```

![](learn_ggplot_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

