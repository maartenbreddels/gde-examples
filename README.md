# Gaia Discovery Engine

This repository contains notebook for exploring the Gaia dataset (1 billion rows, 1 terabyte) using [vaex](https://github.com/vaexio/vaex/) with a remote dataset hosted at AWS. This allows you to compute for instance histograms of the full dataset without having to download all the data. The GDE as a project funded by Heising-Simons Foundation, jointly run by JHU and CMU, with development led by Maarten Breddels.

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

[Voila](https://github.com/QuantStack/voila) makes it possible to share the output of your notebook with others, without showing the code. We have two examples.

## Simple

In this notebook, we use [ipywidgets' interact](https://ipywidgets.readthedocs.io/en/latest/examples/Using%20Interact.html) to make a interactive simple exploration tool.

See a [preview of this notebook on nbviewer](https://nbviewer.jupyter.org/github/maartenbreddels/gde-examples/blob/master/voila-vaex-simple.ipynb)

Or see this screencapture:

![voila-vaex-simple](https://user-images.githubusercontent.com/1765949/65671306-4e272980-e047-11e9-8842-344f559a81e1.gif)

Or [try out the notebook live](http://ec2-18-222-183-211.us-east-2.compute.amazonaws.com:8867/)

You can run this notebook locally (you may want to edit the variable `powerful_machine` to False), by running
```
$ voila ./voila-vaex-simple.ipynb
```


## Advanced

The advanced notebook creates a modern webapp, using [ipyvuetify](https://github.com/mariobuikhuizen/ipyvuetify/) and [bqplot](https://github.com/bloomberg/bqplot). It may be a bit more difficult to understand or modify, but shows how far you can go into building a dashboard using voila, vaex and ipywidgets.

See a [preview of this notebook on nbviewer](https://nbviewer.jupyter.org/github/maartenbreddels/gde-examples/blob/master/voila-vaex-advanced.ipynb)

Or see this screencapture:

![voila-vaex-advanced-opt](https://user-images.githubusercontent.com/1765949/65671611-d4437000-e047-11e9-8af5-f237488b30f0.gif)


Or [try out the notebook live](http://ec2-18-222-183-211.us-east-2.compute.amazonaws.com:8866/voila/render/voila-vaex-gaia-advanced.ipynb)


You can run this notebook locally (only on a powerful machine), by running
 ```
$ voila --enable_nbextensions=True . --template=vuetify-base ./voila-vaex-advanced.ipynb
```
