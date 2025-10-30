--
title: "Developing Data Products - Week 3 Assignment"
author: "Anish Singhal"
output: html_document
---


This document shows an example of making a web presentation with graphics, using *R Markdown* (<http://rmarkdown.rstudio.com>), *Slidy* and *Plotly* (<https://plot.ly/>) together, corresponding to the assignment of *Week 3* of the Developing Data Products course from Coursera (<https://www.coursera.org/learn/data-products>).

Data used by the example is the *Iris Data Set*. This dataset contains 3 classes of 50 instances each, where each class refers to a type of iris plant.

This presentation will show a scatter plot where the *X-Axis* is the column ⁠ Sepal.Length ⁠, the *Y-Axis* is the column ⁠ Sepal.Width ⁠, and the *dots’ colors* are based on the column ⁠ Petal.Length ⁠.

---

## Loading Dataset

⁠ {r}
data("iris")
head(iris)

## Plot

 ⁠{r, message=FALSE, warning=FALSE}
library(plotly)

plot_ly(
  data = iris,
  x = ~Sepal.Length,
  y = ~Sepal.Width,
  type = "scatter",
  mode = "markers",
  color = ~Petal.Length
)
