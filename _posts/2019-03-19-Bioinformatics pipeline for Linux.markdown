---
title:  "Bioinformatics pipeline for Linux"
date:   2019-03-19 2:17
categories: [software, Linux]
tags: [software, setting up, Linux]
---

A to Z.

#### Install Linux

You`re most likely using Win10, so just install the virtual box from Microsoft`s store.

First `sudo apt-get update && apt-get upgrade -y`

`apt-get install -y samtools mafft muscle raxml tabix
apt-get install -y r-bioc-biobase
apt-get install -y graphviz libgraphviz-dev pkg-config  # phylo/biopython
#apt-get install -y swig  # simupop
apt-get install -y libx11-dev
apt-get install -y libgsl0ldbl
apt-get install -y libgsl0-dev libopenblas-dev liblapacke-dev`

`apt-get clean`

#### Install conda

Linux virtual box can only save under the Windows directory. So you're likely using an SSD with limited space, and for some reason you cannot change this. Well, the reason is because it is through the Microsoft Store. In hindsight, I would have installed a separate partition in my actual storage HDD and dual booted. This may pose a problem with upcoming storage hogging genomics data. However, let's move on shall we?

`curl -0 https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh`

We are using the command `curl` to download Anaconda. I chose this version because the only one's available through conda's website are 3.7 and 2.7. 3.7 is a nightmare because, last I checked, Tensorflow does not support it. So I had to dig through legacy versions. It sucked.

Use `sh256sum` to check download integrity.

`sh256sum https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh`

It'll give you a long hashcode, you can use it to see if it`s the same on the website.

Now, let's install this thing.

`bash https://repo.continuum.io/archive/Anaconda3-5.0.1-Linux-x86_64.sh`

`yes` and press enter to confirm the location it's installed on. Add it to your PATH so you can open up conda from anywhere without having to `cd` stuff.

Upgrade it using `conda upgrade conda`, it'll give you a newer version that is still <3.7.

#### Install conda packages

`conda config --add channels bioconda
conda config --add channels bioconda
conda config --add channels r
conda config --add channels conda-forge
conda install --yes biopython=1.70
conda install --yes statsmodels pysam plink gffutils genepop trimal
conda install -c conda-forge simuPOP
conda install --yes pip
conda install --yes rpy2`

`conda install --yes pygraphviz eigensoft
conda install --yes seaborn pexpect pyvcf dendropy networkx reportlab`

`pip install pygenomics`


Now you have most of what you need to conduct bioinformatics tasks in the Linux kernel. Next post will be incorporating Python and R.
