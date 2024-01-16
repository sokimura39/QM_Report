# QM_report

Working repository for CASA0007 written investigation assignment. The submitted report can be found [here](documents/written_work.pdf).

## Structure of code

The analysis is conducted using data from Transport for London (TfL). Each part of the following is conducted in a separate Jupyter notebook.

1. [bike_points.ipynb](bike_points.ipynb) collects docking station data from TfL Unified API, and converts into geospatial data for further analysis
2. [journeys_data_nogeom.ipynb](journeys_data_nogeom.ipynb) collects journey data from TfL data storage, and converts into dataframe for analysis
3. [analysis.ipynb](analysis.ipynb) does the actual analysis

The datasets required for analysis are prepared with the 2 notebooks for data preparation, and should be run in this order to ensure reproducibility.

## Overview of report

This report explores the relationship between the elevation and the journeys taken by the London Cycle Hire Scheme, otherwise known as the Santander Cycles. 

2 perspectives considered for the analysis:

1. The first half focuses on individual docking stations. We explored the ratio between departures and arrivals, assuming that places with high elevation has more journeys starting than terminating
2. The second half focuses on origin-destination pairs of journeys. We considered the impact of height difference to the frequency of journeys from one MSOA to another, assuming downhill journeys occur more frequently than uphills.

## Abstract results

2 main findings from analysis.

##### Docking station analysis

The higher the elevation, the ratio of departures over arrivals was higher, indicating usage taking advantage of downhill journeys.

##### OD pair analysis

No significance can be observed when considering height difference. Distance (or the negative exponential of it) had a dominant effect, and the residuals did not have significant correlation with the height difference.

## Potential future analysis

Considering the cumulative difference, not the origin-destination difference in height, may impact the decisions.


