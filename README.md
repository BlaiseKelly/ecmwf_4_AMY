Using ECMWF reanalysis data for AMY energy modelling files
================
2025-01-05

## Introduction

Numerical weather prediction data (NWP) data such as that available from
ECMWF is very useful for obtaining reliable estimates of historic meteo
conditions for anywhere in the world.

The land reanalysis data has modelled around 30 parameters for every
hour back to 1950 at a resolution of around 7km.

The parameters: - 2m_dewpoint_temperature - 2m_temperature -
soil_temperature_level_1 - snow_cover -
surface_solar_radiation_downwards - 10m_u_component_of_wind -
10m_v_component_of_wind -surface_pressure can be used to derive an
actual meteorological year (AMY) file for any period from 1950 to around
6 months prior to the present.

The API can be obtained by creating a FREE account at
<https://cds.climate.copernicus.eu/>

Once this is done, go to <https://cds.climate.copernicus.eu/profile>,
copy the API key and replace in the script.

to see submitted requests
<https://cds.climate.copernicus.eu/requests?tab=all>

This script downloads the raw meteo data for the parameters above, which
are in netcdf format. The script extracts them and saves as a csv. The
second part converts them to the correct format for the AMY file.

Solar surface downwards radiation

Other tools can be run from R including the openair library, which has
useful plots for visualising meteo data, such as wind roses and calendar
plots.

A full list of all available parameters from the ERA land is availble
here:
<https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land?tab=overview>
Additionally the ERA5 data contains many more parameters, which can be
downloaded using the same script with some small modifications and a
resolution of approximately 30km:
<https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels?tab=overview>
