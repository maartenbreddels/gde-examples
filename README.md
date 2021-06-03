# Gaia Discovery Engine (GDE)

This repository contains notebooks for exploring a remote-hosted Gaia EDR3 x PanSTARRS  dataset (1 billion rows, 1 terabyte) using [vaex](https://github.com/vaexio/vaex/). This system allows you to compute multi-dimensional histograms of the full dataset in _seconds_ without having to download all the data. The GDE as a project funded by the Heising-Simons Foundation through _Scialog_, with PIs Joshua Peek (STScI/JHU) and Sergey Koposov (Edinburgh) and development led by Maarten Breddels.



# The notebooks

## Intro to Vaex using Gaia EDR3 data

`10-introduction-vaex-gaia.ipynb` will learn you how to use vaex to connect to the remote dataset/dataframe with an API similar to Pandas. We will go through a basic workflow to show you how you can use vaex for data exploration.

[![preview on nbviewer](https://img.shields.io/badge/preview%20with-%20nbviewer-rgb(228,110,46))](https://nbviewer.jupyter.org/github/maartenbreddels/gde-examples/blob/master/10-introduction-vaex-gaia.ipynb)
 [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/maartenbreddels/gde-examples/HEAD?filepath=10-introduction-vaex-gaia.ipynb)


## Simple Voilà dashboard showing a HR Diagram.

`20-voila-vaex-hr-diagram.ipynb` shows how to create a simple interactive dashboard showing a Hertzsprung-Russell (HR) diagram

[![Voila](https://img.shields.io/badge/run%20with-%20voilà-rgb(93,188,175))](https://voila.vaex.io/voila/render/gde-examples/20-voila-vaex-hr-diagram.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/maartenbreddels/gde-examples/HEAD?filepath=20-voila-vaex-hr-diagram.ipynb)


## Full interactive Voilà dashboard showing a HR Diagram and Sky map.

`30-voila-vaex-sky-hr-diagram.ipynb` shows how to create a fully interactive dashboard with a Sky plot and a Hertzsprung-Russell (HR) diagram

[![Voila](https://img.shields.io/badge/run%20with-%20voilà-rgb(93,188,175))](https://voila.vaex.io/voila/render/gde-examples/30-voila-vaex-sky-hr-diagram.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/maartenbreddels/gde-examples/HEAD?filepath=30-voila-vaex-sky-hr-diagram.ipynb)




# How to run the notebooks locally

Assuming conda (otherwise see http://vaex.io/docs/installing.html), run the following commands:

```shell
$ git clone https://github.com/maartenbreddels/gde-examples
$ cd gde-examples

# assuming conda
$ conda -c conda-forge install vaex-core vaex-hdf5 vaex-viz vaex-server notebook voila

# otherwise using pip:
# $ pip install -r requirements.txt

# to run the notebook
$ jupyter notebook

# to run the dashboard
$ voila 30-voila-vaex-sky-hr-diagram.ipynb
```
