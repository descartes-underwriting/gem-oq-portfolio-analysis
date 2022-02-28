# gem-oq-portfolio-analysis


# Portfolio Accumulation

We want to analyze the impact of new locations onto an existing portfolio.
For that we prepared the following folders & files:


- `hazard_model`: contains the open-source `ZAF v2018` hazard model that is used in the following

- `first_run`:
  - `sites1.csv`: contains the two locations that simulate the existing portfolio,
  - `AccumulationTest1.zip`: contains the complete run configuration, with the `hazard_model` and the locations of `sites1.csv`
  - `calc_46.hdf5`: contains the result of the event-based run with the `ZAF v2018` model and the locations of `sites1.csv`

- `second_run`:
  - `sites2.csv`: contains 4 new locations of which we want to know the correlation with our existing portfolio (= `sites1.csv`)
  - `AccumulationTest2.zip`: contains the run configuration (tbc) to analyze the impact onto our portfolio

## Event-based runs with preset Ruptures

To analyze the correlation of the 4 new locations onto the existing 2 locations,

### Same rupture samples

we want to re-use the same sampled ruptures of the `first_run`.
Preferably we want to use the `calc_46.hdf5`

_How do we have to adjust the `job.ini` file to do so?_


### Same GMPE samples

we want to re-use the same sampled GMPEs of the `first_run`s.
Preferably we want to use the `calc_46.hdf5`

We want to be able to do this in two ways:
1. Keep the same GMPEs for the same realization, but vary the sampled $\sigma_i$ of the truncation level for each event.
2. Keep the same GMPEs _and_ the same $\sigma_i$ of the truncation level for all the events. 

_How do we have to adjust the `job.ini` file to do so?_



# V3.13-Problems 


