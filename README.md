# Gaia Discovery Engine

This repository contains notebook for exploring the Gaia dataset (1 billion rows, 1 terabyte) using [vaex](https://github.com/vaexio/vaex/) with a remote dataset hosted at AWS by [STScI](http://www.stsci.edu). This allows you to compute for instance histograms of the full dataset without having to download all the data.

# Installation/running

Assuming conda (otherwise see http://docs.vaex.io/en/latest/installing.html), run the following commands:

```
$ conda -c conda-forge install vaex-core vaex-hdf5 vaex-viz notebook voila
$ git clone https://github.com/maartenbreddels/gde-examples
$ cd gde-examples
$ jupyter notebook
```


# Introduction

Open `introduction-vaex-gaia.ipynb` in Jupyter notebook (or Jupyter lab) to learn how to use vaex to connect to the remote dataset/dataframe with an API similar to Pandas. We will go through a basic workflow to show you how you can use vaex for data exploration

See a [preview of this notebook on nbviewer](https://nbviewer.jupyter.org/github/maartenbreddels/gde-examples/blob/master/introduction-vaex-gaia.ipynb)

Or see this screencapture:

![introduction-vaex-gaia](https://user-images.githubusercontent.com/1765949/65245603-27b83a00-daed-11e9-968a-9fda75582d89.gif)


# Voila

