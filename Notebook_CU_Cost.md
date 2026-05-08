## Scenario

As a user, I want to calculate the cost of an individual notebook run, and ideally I want to do this at scale for a number of notebooks. 


### Outline Solution

This work builds on FUAM core notebooks. Thanks to Erik Bohn and Viktor Dudas for their DAX and notebook help.

Assumptions:  
   - Capacity Metrics App (CapMetrics) is installed and refreshing daily
   - Capactity Metrics semantic model is accessible to the appropriate user
   
Approach:

Detailed data about particular item operations is available in the CapMetrics report, via the timepoint drill throughs. By iterating through the available timepoints, extract detailed operation data and compile CUs consumed by operation in the Timepoints.

For Notebooks, used Stopped status to harvest information on total duration and CUs. This may be captured in multiple timepoints, so use only the most recent timepoint row for this information.

### Solution Detail Steps

1. Capture a list of available Capacities and filter to just one Capacity, capture all the timepoints within a specified range [Admin notebook 1](/notebooks/nb_admin_0200_CollectCapacityMetrics.ipynb)
2. Use the result of Notebook 1 to iterate through each of the timepoint details and capture operation data [Admin notebook 2](/notebooks/nb_admin_0220_CollectCapacityMetricsTimepointDetail.ipynb) 
3. Explore the resulting data, inputting regions and costs for Capacity and billing type [Admin notebook 3](/notebooks/nb_admin_0240_CUMetricsExplorer.ipynb) 