---
title: '`FitBenchmarking`: an open source `Python` package comparing data fitting software'
tags:
  - Python
  - fitting
  - non-linear least squares
authors:
  - name: Tyrone Rees
    affiliation: 1
  - name: Anders Markvardsen
    affiliation: 1
  - name: Michael Wathen
    affiliation: 1
  - name: Andrew Lister
    affiliation: 1
  - name: Patrick Odagiu
    affiliation: 1
  - name: Atom Anuchitanukul
    affiliation: 1
  - name: Tom Farmer
    affiliation: 1
  - name: Anthony Lim
    affiliation: 1
  - name: Federico Montesino
    affiliation: 1
  - name: Tim Snow
    affiliation: 2
  - name:  Andrew McCluskey
    affiliation: 2
affiliations:
 - name: STFC Rutherford Appleton Laboratory
   index: 1
 - name: Diamond light source
   index: 2
date: October 2020
bibliography: paper.bib
---
# Summary

Fitting a mathematical model to data is a fundamental task across all scientific disciplines. [`FitBenchmarking`](https://fitbenchmarking.com/) has been designed to to help:

* Scientists, who want to know what is the best algorithm for fitting their model to data they might encounter, on their specific hardware;
* Scientific software developers, who want to know what is the state-of-the-art in fitting algorithms and implementations, what they should recommend as their default solver, and if they should implement a new method in their software; and
* Mathematicians and numerical software developers, who want to understand the types of problems on which current algorithms do not perform well, and to have a route to expose newly developed methods to users.

Representatives of each of these communities have got together to build `FitBenchmarking`. We hope this tool will help foster fruitful interactions and collaborations across the disciplines.

![Benchmarking paradigm \label{fig:concept}](figures/FitBenchmarkingConcept.png){width=60%}

`FitBenchmarking` is easy to install via `pip` and our [documentation](https://fitbenchmarking.com/) guides users through the installation of some external packages we support. We provide several data sets from a range of applications and adding new data in these formats is as easy as dropping the data into a new folder. The data and fitting packages currently supported are shown in Figure \ref{fig:concept}. A key part of `FitBenchmarking` is the ease of which a user, with a basic knowledge of `Python`, can add new fitting software, data formats and different fitting comparison output metrics.

# Statement of need

`FitBenchmarking` originally started as a tool to benchmark minimizers in the data analysis package `Mantid` [@mantid], which was designed for neutron scattering and muon spectroscopy data. `FitBenchmarking` has since been significantly extended to take data and models from real world applications and data analysis packages, such as `SasView` [@sasview] and `CUTEst` [@cutest]. It fits models to the data by using a range of data fitting and nonlinear optimization software packages, and present comparisons through a variety of different metrics. These include comparison tables and performance profile plots.

Figure \ref{fig:sample} displays a data set from `FitBenchmarking` where the crosses are the data points and the two curves are fitted models using two minimizers from `GSL` [@gsl]. The fitting package finds the best parameters for the model by solving a nonlinear least-squares problem. From Figure \ref{fig:sample}, it is clear that the solution given by lmsder is better. As the volume of data increases, and we do more and more data analysis algorithmically, it is increasingly important that we have the best algorithm without needing to check it by eye. `FitBenchmarking` generates HTML output that makes it easy to compare minimizers on a given problem set.

![A sample fit \label{fig:sample}](figures/nmsimplex2_fit_for_EVS14188-90_processed_Gaussian_peaks_1_1.png){width=70%}

`FitBenchmarking` will help the scientist make an informed choice by comparing runtime and accuracy of all available minimizers, on their specific hardware, on problems from their science area.

`FitBenchmarking` will help the scientific software developer ensure that the most robust and quickest algorithms for the type of data analysis they support are available in their software.

`FitBenchmarking` will help mathematicians see what the state of the art is, and what kinds of data are problematic. It will give them access to real data, and will give a route for novel methods to quickly make it into production.

# Acknowledgements

We also would like to acknowledge funding support from:

* European Union’s Horizon2020 research and innovation programme, EU SINE2020 WP-10,
* EPSRC Grant EP/M025179/1 -- Least Squares: Fit for the Future.
* The Ada Lovelace Centre (ALC).

# References