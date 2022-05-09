# gem-oq-portfolio-analysis: Portfolio Accumulation

## Description

We carried out two events-based PHA analyses using the same hazard input model (`ZAF v2018`):
- first run: contains the input and output of an event based PSHA analysis for a single site with coordinates (-34.094, 18.387)
- second run: contains the input and output of an event based PSHA analysis for a single site with coordinates (-34.005, 18.503)

The list of simulated ruptures is different in the two analyses (see respectively `first_run\output\output-204-ruptures_49.csv` and `second_run\output\output-216-ruptures_51.csv`).

We would like to run event-based PSHA analyses using the same list of ruptures for both cases (`first_run` and `second_run`).

Ideally we would like to run openquake analyses with a list of ruptures externally provided as an input.