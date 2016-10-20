# Identikit Models

A library of hybrid N-body + test particle simulations for dynamical modeling of galaxy interactions.
These are intended for use within the [Identikit](http://www.ifa.hawaii.edu/faculty/barnes/research/identikit/index.html) environment.

This repository consists of bulge+disk+NFW halo galaxy models to facilitate exploration of encounters with various mass ratios.
The "full mass" and "half mass" models are the same as those provided by [Barnes & Hibbard (2009)](http://adsabs.harvard.edu/abs/2009AJ....137.3071B) and the makefiles are adapted from those provided with Identikit.

The "quarter mass" and "eighth mass" models have been created by George Privon.
These models were computed by further reducing the scale lengths by a factor sqrt(2) for each halving of the mass.

The initial conditions files given below provide sample encounters for parabolic orbits and a variety of pericenter seperations.

## Software Requirements

Running these simulations requires installation of the [Zeno N-body/SPH simulation environment](http://www.ifa.hawaii.edu/faculty/barnes/zeno/) ([github link](https://github.com/joshuabarnes/zeno)).

## Files

### Initial Conditions and Run Files

The initial conditions files and run files follow a naming convention of `IdkZYX` and `IdkZYXrun`, where the numbers replacing ZYX correspond to:

* `Z` = 1 indicating parabolic orbits
* `Y` indicating the sum of the fractional masses of the interacting galaxies. `2` indicates and equal-mass encounter (`1+1`) while `5` indicates a 1:4 mass ratio (`1+4`).
* `X` indicates the pericenter separation at first pass, for the idealized Keplerian orbit. This corresponds to multiples of `1/16` simulation units.

Thus, `Idk12X` contains initial conditions for equal mass galaxy encounters on parabolic orbits.
The file has a range of first pericenter encounters.
The `Idk12Xrun` file contains routines to evolve the initial conditions for a suitable time range and save the snapshots for comparison with data.

### Support Files

* `halo_...` Halo mass profiles, accounting for the [effects of gravitational softening](http://www.ifa.hawaii.edu/faculty/barnes/research/smoothing/).
* `bulge_...` Hernquist bulge mass profiles, accounting for the [effects of gravitational softening](http://www.ifa.hawaii.edu/faculty/barnes/research/smoothing/).

## Citations

Users of these models should cite [Barnes & Hibbard (2009)](http://adsabs.harvard.edu/abs/2009AJ....137.3071B).
