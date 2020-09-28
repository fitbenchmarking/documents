---
title: '`FitBenchmarking`'
tags:
  - Python
  - fitting
  - non-linear least squares
authors:
  - name: Atom Anuchitanukul
    affiliation: 1
  - name: Tom Farmer
    affiliation: 1
  - name: Anthony Lim
    affiliation: 1
  - name: Andrew Lister
    affiliation: 1
  - name: Anders Markvardsen
    affiliation: 1
  - name:  Andrew McCluskey
    affiliation: 2
  - name: Patrick Odagiu
    affiliation: 1
  - name: Tyrone Rees
    affiliation: 1
  - name: Tim Snow
    affiliation: 2
  - name: Michael Wathen
    affiliation: 1
affiliations:
 - name: STFC Rutherford Appleton Laboratory
   index: 1
 - name: Diamond light source
   index: 2
date: September 2020
bibliography: paper.bib
---
# Summary

[`FitBenchmarking`](https://fitbenchmarking.com/) is a tool which compares multiple different software packages for non-linear least squares fitting on several problem sets. This project was original written to benchmark Mantid minimizers [@mantid] for neutron and muon scattering data sets. However, fitting a mathematical model to data is a fundamental task across all scientific disciplines. (At least) three groups of people have an interest in fitting software:

* Scientists, who want to know what is the best algorithm for fitting their model to data they might encounter, on their specific hardware;
* Scientific software developers, who want to know what is the state-of-the-art in fitting algorithms and implementations, what they should recommend as their default solver, and if they should implement a new method in their software; and
* Mathematicians and numerical software developers, who want to understand the types of problems on which current algorithms do not perform well, and to have a route to expose newly developed methods to users.

Representatives of each of these communities have got together to build FitBenchmarking. We hope this tool will help foster fruitful interactions and collaborations across the disciplines.

FitBenchmarking takes data and models from real world applications and data analysis packages, such as Mantid [@mantid] and CUTEst [@cutest]. It fits the data to the models by casting them as a nonlinear least-squares problem. We fit the data using a range of data fitting and nonlinear optimization software, and present comparisons through a variety of different metrics. One of the main concepts behind FitBenchmarking is how
![Concept](../../fitbenchmarking/docs/images/FitBenchmarkingConcept.png){ width=50%,align=center}

<!-- When fitting a function to experimental or simulated data, the minimizer is the
method that adjusts the function parameters so that the model fits the data as
closely as possible. The concept of how close a fit is to the data is defined by
the cost function. The cost function is defined as follows:
$$\sum_i \left(\frac{y_i^{\text{obs}} - y_i^{}}{\sigma_i}\right)^2.$$
where $y_i$ is shorthand for $y(x_i)$, i.e. the $y$-value calculated at the observed value $x_i$ from a model,
and $y_i^{\text{obs}}$ and $\sigma_i$ are the observed value and observed/estimated error value at $x_i$ respectively.
 -->

FitBenchmarking will help the scientist make an informed choice by comparing runtime and accuracy of all available minimizers, on their specific hardware, on problems from their science area, which will ensure they are using the most appropriate minimizer.

FitBenchmarking will help the scientific software developer ensure that the most robust and quickest algorithms for the type of data analysis they support are available in their software.

FitBenchmarking will help mathematicians see what the state of the art is, and what kinds of data are problematic. It will give them access to real data, and will give a route for novel methods to quickly make it into production.

# Acknowledgements

We also would like to acknowledge funding support from:

* European Union’s Horizon2020 research and innovation programme, EU SINE2020 WP-10,
* EPSRC Grant EP/M025179/1 -- Least Squares: Fit for the Future.
* The Ada Lovelace Centre (ALC).

# References
