# gem-oq-portfolio-analysis: Portfolio Accumulation

## Goal Description

We want to analyze the impact of new locations onto an existing portfolio.

## Content Description

We prepared the following folders & files:

- `hazard_model`: contains the open-source `ZAF v2018` hazard model that is used in the following

- `first_run`:
  - `sites1.csv`: contains the two locations that simulate the existing portfolio,
  - `AccumulationTest1.zip`: contains the complete run configuration, with the `hazard_model` and the locations of `sites1.csv`
  - `calc_46.hdf5`: contains the result of the event-based run with the `ZAF v2018` model and the locations of `sites1.csv`

- `second_run`:
  - `sites2.csv`: contains 4 new locations of which we want to know the correlation with our existing portfolio (= `sites1.csv`)
  - `AccumulationTest2.zip`: contains the run configuration (tbc) to analyze the impact onto our portfolio

## Wanted-Outcome Description

### Event-based runs with preset Ruptures

Our goal is to run an Event-based PSHA analysis for the second group of assets (i.e. sites2.csv) under the same assumptions as for the first group of assets (i.e. sites1.csv).

Preferably, based on the sampled ruptures of `firs_run`, only the ground motion fields at the set of `sites2.csv` is calculated.

To analyze the correlation of the 4 new locations onto the existing 2 locations:

#### 1.  Variable truncation samples

```bash
How to give the same list of rupture to the assets

* @maria : reword the paragraph
* @bernie : have an example ?
* @fred : find the middle ground in the text
```

We want to re-use the same sampled ruptures and the same GPMEs of the `first_run`.
Preferably we want to use the `calc_46.hdf5` file.

Fixed Variables:

- Realizations
- Events
- Ruptures

Flexible Variables:

- Sampled stds of the truncation level

_How do we have to adjust the `job.ini` file in `AccumulationTest2.zip` to do so?_

#### 2. Fixed truncation samples

We want to re-use the same sampled ruptures and the same GPMEs of the `first_run`.
Preferably we want to use the `calc_46.hdf5` file.
On top, we want to use the same sampled truncations of the GMPEs.

Fixed Variables:

- Realizations
- Events
- Ruptures
- Sampled stds of the truncation level

Flexible Variables:

- None

_How do we have to adjust the `job.ini` file in `AccumulationTest2.zip`  to do so?_
