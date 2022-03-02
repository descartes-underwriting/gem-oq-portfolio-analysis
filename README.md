# gem-oq-portfolio-analysis


# Portfolio Accumulation

## Goal

We would like to analyze the impact of new locations onto an existing portfolio.

## Use case
For that we prepared the following folders & files:

- `hazard_model`: contains the open-source `ZAF v2018` hazard model that is used in the following

- `first_run`:
  - `sites1.csv`: contains the two locations that simulate the existing portfolio,
  - `AccumulationTest1.zip`: contains the complete run configuration, with the `hazard_model` and the locations of `sites1.csv`
  - `calc_46.hdf5`: contains the result of the event-based run with the `ZAF v2018` model and the locations of `sites1.csv`

- `second_run`:
  - `sites2.csv`: contains 4 new locations of which we want to know the correlation with our existing portfolio (= `sites1.csv`)
  - `AccumulationTest2.zip`: contains the run configuration (tbc) to analyze the impact onto our portfolio

## What we would like to achieve: Event-based PSHA analysis with the same assumptions

Our goal is to run an Event-based PSHA analysis for the second group of assets (i.e. `sites2.csv`) using the same assumptions used for the Event-based PSHA run with the first group of sites (i.e. `sites1.csv`)
This would allow us to directly accounting for the correlation of new assets (in this example 4 locations) added to our preexisting portfolio (in this example 2 locations).

More specifically, to achieve this goal we would like to use the same realizations for the two runs. Of course for each realizations we would like to use: 
1. the same ruptures
2. the same GMPE associated to each rupture

### Same rupture samples

For each realization, we would like the same sampled ruptures of the `first_run`.
Preferably we would like to use the `calc_46.hdf5` file.

_How do we have to adjust the `job.ini` file in `AccumulationTest2.zip` to do so?_
_Do we have to define other input files to do so?_


### Same GMPE samples

For each rupture of the previous point, we would like to re-use the same sampled GMPEs of the `first_run`.
Preferably we would like to use the `calc_46.hdf5` file.

If possible, we would like to be able to do this in two ways:
1. Without any groundmotion spatial correlation model
2. With a groundmotion spatial correlation model. This, we guess, requires to save besides the GMPE also the information of the sampled sigma of the first run (This second option is definitively not high priority)

_How do we have to adjust the `job.ini` file in `AccumulationTest2.zip` to do so?_


# V3.13-Problems 


