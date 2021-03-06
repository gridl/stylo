# stylo: R package for stylometric analyses

**Authors:** Maciej Eder, Mike Kestemont, Jan Rybicki<br/>
**License:** [GPL-3](https://opensource.org/licenses/GPL-3.0)


[![CRAN Version](http://www.r-pkg.org/badges/version/stylo)](https://CRAN.R-project.org/package=stylo) [![Travis-CI Build Status](https://travis-ci.org/computationalstylistics/stylo.svg?branch=master)](https://travis-ci.org/computationalstylistics/stylo) [![CRAN Downloads](http://cranlogs.r-pkg.org/badges/grand-total/stylo)](https://www.rpackages.io/package/stylo) ![Downloads](http://cranlogs.r-pkg.org/badges/stylo)


This package provides a number of functions, supplemented by a GUI, to perform various
analyses in the field of computational stylistics, authorship attribution, etc.






## Citation

If you find the package `stylo` useful and plan to publish your results, please consider citing the following paper:

**Eder, M., Rybicki, J. and Kestemont, M.** (2016). Stylometry with R: a package for computational text analysis. _R Journal_, 8(1): 107-21.  [https://journal.r-project.org/archive/2016/RJ-2016-007/index.html](https://journal.r-project.org/archive/2016/RJ-2016-007/index.html)





## Installation

There are three ways of installing `stylo`:

* from CRAN repository
* from the GitHub repository, via the package `devtools`
* from a locally downloaded file






###  1. Installing from CRAN

Launch R, make sure you are connected to the internet, type: 

```
install.packages("stylo")
```

choose your favorite CRAN mirror (a window will pop up), click OK.

**NOTE** (Mac OS users): the package "stylo" requires X11 support being installed. To quote "R for Mac OS X FAQ" (http://cran.r-project.org/bin/macosx/RMacOSX-FAQ.html): "Each binary distribution of R available through CRAN is build to use the X11 implementation of Tcl/Tk. Of course a X windows server has to be started first: this should happen automatically on OS X, provided it has been installed (it needs a separate install on Mountain Lion or later). The first time things are done in the X server there can be a long delay whilst a font cache is constructed; starting the server can take several seconds." The newest versions of R (>3.1.0) seem to have Tcl/Tk support out-of-the-box, though.

**ANOTHER NOTE** (Mac Os users again): when you install a recent version of R on OS X (e.g. Mavericks), you might run into encoding errors when you start up R (e.g. "WARNING: You're using a non-UTF8 locale" etc.). In that case, you should close R, open a new window in Applications > Terminal and execute the following line:


```
defaults write org.R-project.R force.LANG en_US.UTF-8
```

Next, close the Terminal and start up R again.





### 2. Installing from the GitHub repository

A convenient way to install R packages directly from the GitHub repository is to use the package `devtools`. Unless you have already installed it, you should do it now:

```install.packages("devtools")```

Then, install the package `stylo`

```
library(devtools)
install_github("computationalstylistics/stylo")
```





### 3. Installing from a local file

Download the package from **here**; save the file anywhere on your computer where you will be able to find it; launch R; set working directory to the folder where the downloaded file is (please keep it mind that the slashes might look different in different operating systems):

```
setwd("i/hope/i/can/remember/where/it/was/")
```

Install the package:

```
install.packages("stylo_0.6.5.tar.gz", repos = NULL, type = "source")
```

**NOTE**: the `stylo` package requires a few standard R packages to be installed. When installing from CRAN or from GitHub, the dependencies are downloaded automatically; otherwise, you have to install them manually. Type (or copy-paste) the following lines:

```
install.packages("tcltk2")
install.packages("ape")
install.packages("class")
install.packages("e1071")
install.packages("pamr")
install.packages("tsne")
```



## Usage

This section is meant to give the users a general outline of what the package can do, rather than providing a comprehensive description of designing a stylometric test using the R package `stylo`. Refer to the following documents:

* for (real) beginners: a crush introduction in the form of a [slideshow](https://computationalstylistics.github.io/stylo_nutshell/)
* for (sort of) beginners: a concise [HOWTO](https://sites.google.com/site/computationalstylistics/stylo/stylo_howto.pdf)
* for advanced users: a paper in [R Journal](https://journal.r-project.org/archive/2016/RJ-2016-007/RJ-2016-007.pdf)
* full documentation at [CRAN](https://cran.r-project.org/web/packages/stylo/stylo.pdf)






## Docs on non-obvious functions


* [Authorship verification with the package 'stylo'](https://computationalstylistics.github.io/docs/imposters)

* [Cross-validation using the function `classify()`](https://computationalstylistics.github.io/docs/cross_validation)

* [Custom distance measures](https://computationalstylistics.github.io/docs/custom_distances)

* [Testing rolling stylometry](https://computationalstylistics.github.io/docs/rolling_stylometry)







## Other relevant resources


* Despite a black legend, R and Python are not necessarily in a deadly clash: here is [a great post](https://cligs.hypotheses.org/577) by José Calvo Tello on invoking the package `stylo` directly from Python!

* Using the package `stylo` with the TXM environment: see [this post](https://groupes.renater.fr/wiki/txm-users/public/tutorial_to_use_stylo_into_txm) by Serge Heiden.

* Probably not a  bad idea to check a comprehensive [Stylometry Bibliography](https://www.zotero.org/groups/643516/stylometry_bibliography) curated by Christof Schöch, before starting an experiment in text analysis.

* The package `stylo` has been created as a by-product of a few projects conducted by the Computational Stylistics Group. See  [this website](https://sites.google.com/site/computationalstylistics/) for further details.



