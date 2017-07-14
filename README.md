# Weathering Simulations


This repository contains a collection of weathering simulations.

The degradation of polyethylene terephthalate (PET) is modeled
using a variety of Typical Meteorological Year data sets from NREL.

#### Data
The data sets can be found here:
http://rredc.nrel.gov/solar/old_data/nsrdb/1991-2005/tmy3/by_state_and_city.html

And the users guide here:
http://www.nrel.gov/docs/fy08osti/43156.pdf

#### Pre-processing

There are two notebooks for cleaning the data and loading it into a MySQL database.

1. <b>format_NREL_data.ipynb</b>

    Converts the 01-24 range for the hours into 00-23 required by SQL DATETIME and python datetime.

2. <b>NREL_to_MySQL.ipynb</b>

    Creates a table named after the CSV data file and loads the data CSV from the CSV file.  It requires the output from format_NREL_data.ipynb, not the raw NREL files.

#### Simulations

1. <b>basic_weathering_year.ipynb</b>

    Runs a one year simulation for a specified location.  Calculates basic Arrhenius model of PET degradation.  Plots and reports results.

2. <b>basic_weathering_year.ipynb</b>

     Runs a one month simulation for a specified location.  Calculates basic Arrhenius model of PET degradation.  Plots and reports results.
