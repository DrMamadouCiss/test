Affichage graphique: niveau 1
================
Dr Mamadou Ciss

14 janvier 2019
================


-   [Fichier initial](#fichier-initial)
-   [Nuage de points](#nuage-de-points)
-   [Boxplots](#boxplots)
-   [Histogramme](#histogramme)
-   [Diagramme en bandes](#diagramme-en-bandes)
-   [Diagramme en barres](#diagramme-en-barres)
-   [Diagramme circulaire](#diagramme-circulaire)

Fichier initial
---------------

``` r
str(iris)
```

    ## 'data.frame':    150 obs. of  5 variables:
    ##  $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
    ##  $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
    ##  $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
    ##  $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
    ##  $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...

``` r
head(iris)
```

    ##   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
    ## 1          5.1         3.5          1.4         0.2  setosa
    ## 2          4.9         3.0          1.4         0.2  setosa
    ## 3          4.7         3.2          1.3         0.2  setosa
    ## 4          4.6         3.1          1.5         0.2  setosa
    ## 5          5.0         3.6          1.4         0.2  setosa
    ## 6          5.4         3.9          1.7         0.4  setosa

``` r
tail(iris)
```

    ##     Sepal.Length Sepal.Width Petal.Length Petal.Width   Species
    ## 145          6.7         3.3          5.7         2.5 virginica
    ## 146          6.7         3.0          5.2         2.3 virginica
    ## 147          6.3         2.5          5.0         1.9 virginica
    ## 148          6.5         3.0          5.2         2.0 virginica
    ## 149          6.2         3.4          5.4         2.3 virginica
    ## 150          5.9         3.0          5.1         1.8 virginica

Nuage de points
---------------

``` r
plot(iris$Petal.Width~iris$Petal.Length)
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-2-1.png)

``` r
plot(iris$Petal.Width~iris$Petal.Length,xlab='Longueur petal',ylab='Largeur petal' )
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-3-1.png)

Boxplots
--------

``` r
boxplot(iris)
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-4-1.png)

Histogramme
-----------

``` r
hist(iris$Petal.Width)
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-5-1.png)

Diagramme en bandes
-------------------

``` r
tabb=table(iris$Species)
barplot(tabb,col='red')
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-6-1.png)

Diagramme en barres
-------------------

``` r
plot(tabb,col='red',type='h')
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-7-1.png)

Diagramme circulaire
--------------------

``` r
pie(tabb)
```

![](affichage_graphique1_files/figure-markdown_github/unnamed-chunk-8-1.png)
