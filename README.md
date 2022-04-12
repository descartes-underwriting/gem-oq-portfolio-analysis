# gem-oq-portfolio-analysis: Portfolio Accumulation

## Goal Description

We want to analyze the impact of new locations onto an existing portfolio.

## Content Description

We prepared the following folders & files:

- `hazard_model`: contains the open-source `ZAF v2018` hazard model that is used in the following

- `current_portfolio_run`:
  - `sites1.csv`: contains the two locations that simulate the existing portfolio,
  - `AccumulationTest1.zip`: contains the complete run configuration, with the `hazard_model` and the locations of `sites1.csv`
  - `calc_46.hdf5`: contains the result of the event-based run with the `ZAF v2018` model and the locations of `sites1.csv`

- `additional_deal_run`:
  - `sites2.csv`: contains 4 new locations of which we want to know the correlation with our existing portfolio (= `sites1.csv`)
  - `AccumulationTest2.zip`: contains the run configuration (tbc) to analyze the impact onto our portfolio

## Wanted-Outcome Description

### 1. Event-based runs with preset Ruptures

Our goal is to run an Event-based PSHA analysis for the second group of assets (i.e. sites2.csv) under the same assumptions as for the first group of assets (i.e. sites1.csv).

More specifically, we would like to use for the `additional_deal_run`, the same sampled ruptures of the `current_portfolio_run`.

_How do we have to adjust the `job.ini` file and the input files in `AccumulationTest2.zip` to do so?_

### 2.  Event-based runs with the same GMPE associated to each Rupture

Once able to use the same samples of ruptures of the `current_portfolio_run` for the `additional_deal_run` as described above, we would like to use for each sampled rupture the same GMPE used in the `current_portfolio_run` also for the `additional_deal_run`.

_How do we have to adjust the `job.ini` file and the input files in `AccumulationTest2.zip` to do so?_

In other words, for the two runs (i.e. `current_portfolio_run` and `additional_deal_run`) we would like to use the same realizations. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

