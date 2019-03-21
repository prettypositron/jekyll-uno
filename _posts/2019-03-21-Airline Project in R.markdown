---
title:  "Airplane Project with R; Some info about my build"
date:   2019-03-19 7:52AM
categories: [software, R, build]
tags: [software, setting up, R, buildguide]
---

#### Airline Projec

[Airline Project](https://prettypositron.github.io/minimal/Airline%20Project.html)

I'm using a dataset obtained from planespotters.net

It is a work in progress, as I need to single out the Boeing 737 MAX 8, which is the type that has been crashing.

[Here](https://www.planespotters.net/production-list/Boeing/737/737-MAX-8) is a page about the specific airplane.

I'm using this as an opportunity to learn R, so this was all coded using the R kernel in Jupyter Notebook.



#### Install R

I just installed the latest non-beta one from their website (Win10, 64-bit). It's a bit annoying installing batch packages (can't seem to do them, and the package manager in the GUI is awful), but I set up R using:

`install.packages("ggplot2", "readr", "dplyr", "stringr")`

Until I figure out a way to install batch packages from CRAN, I will have to download them piece-meal as I need them.

#### What is your build

In case anyone was wondering, these are the specs for my current rig. Disregard the high CPU temperature as it is a misread. The CPU temp is between 29-35 degrees.:
![](https://prettypositron.github.io/minimal/images/speccy.PNG)

Here's also my [build guide](https://pcpartpicker.com/guide/JcLrxr/deep-learning-and-gaming-rig) and corresponding [build](https://pcpartpicker.com/b/zdTBD3)

It's PCMark Benchmark:![](https://prettypositron.github.io/minimal/images/pcmark10.PNG)

Some pretty pictures as well:

![](https://prettypositron.github.io/minimal/images/IMG_20190314_192354.jpg)
![](https://prettypositron.github.io/minimal/images/IMG_20190314_192434.jpg)
![](https://prettypositron.github.io/minimal/images/IMG_20190314_192437.jpg)
![](https://prettypositron.github.io/minimal/images/IMG_20190314_192441.jpg)
![](https://prettypositron.github.io/minimal/images/IMG_20190314_193114.jpg)
![](https://prettypositron.github.io/minimal/images/IMG_20190314_193124.jpg)
![](https://prettypositron.github.io/minimal/images/IMG_20190314_193130.jpg)

#### Next Step

Next step is to obtain a dataset for Boeing stocks historic trends and compare them to Boeing crashes.

I can foresee a few things that may happen:

Boeing may be "too big to fail" considering how they are the sole US manufacturers of airplanes, and how this is the second crash in a month. There may also be diplomatic tension with China especially during an election year (coming election year) and protectionist sentiment. If I had the capital, I would short it at the end of this green bubble, or simply purchase the stock as it is undervalued right now.

![](https://prettypositron.github.io/minimal/images/boeing.jpg)
