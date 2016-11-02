Homework 4
================

You are currently in the GitHub repository (repo) for `HW-4`. You must have completed all the steps in [Setting Up](https://rudeboybert.github.io/MATH216/jekyll/update/2016/09/12/getting-started.html).

Learning Goals
--------------

-   Working with choropleth maps in R
-   Tackling a larger-scale more open-ended question

Homework
--------

1.  Follow the same workflow as in <a target="_blank" class="page-link"
    href="https://github.com/2016-09-Middlebury-Data-Science/HW-0#homework">HW-0</a> for HW-4.
2.  Do not submit a `HW-4.Rmd` file that does not knit.
3.  I anticipate you spending between 8-12 total (across all submissions) on this homework.

Tips
----

-   Use the 2010 Census data; missing data should not be a problem except for [Fairfax County, Virginia](http://www.census.gov/quickfacts/table/PST045215/51059) with FIPS Code 51059.
-   One-dimensional [center of mass](http://hyperphysics.phy-astr.gsu.edu/hbase/imgmec/cm.gif)
-   To get the [centroid](https://en.wikipedia.org/wiki/Centroid) of a `SpatialPolygons` class object in R, use `sp::coordinates()` which returns a matrix where the first column is longitude and the second is latitude. You can assume that the order of the centroids matches the order of `counties_sp@data` in the example below:

``` r
library(USAboundaries)
library(sp)

counties_sp <- us_counties()
centroids <- coordinates(counties_sp)
head(centroids)
```

    ##         [,1]     [,2]
    ## 0 -116.60176 48.29976
    ## 1  -85.42674 41.64232
    ## 2 -121.64454 45.51723
    ## 3  -97.69895 27.42438
    ## 4  -87.77990 36.03963
    ## 5  -97.85142 34.48557
