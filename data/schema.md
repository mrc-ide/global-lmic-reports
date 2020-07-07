## Data Schema

* **date** - ISO Date for the predicted number of infection/deaths/hospital burden
* **compartment** - One of deaths, infections, hospital demand and  ICU demand or Rt
* **y_025, y_25, y_median, y_mean, y_75, y_975** - Summary statistics for the compartment. E.g. y_25 is the 25% quantile
* **scenario** - The intervention scenario explored. One of Maintain Status Quo, Additional 50% Reduction, Relax Interventions 50%. Surged Maintain Status Quo also present in countries estimated to pass capacity in next 28 days.
* **country** - Country name
* **iso3c** - Country ISO3C letter
* **report_date** - ISO Date at which the reports were generated, i.e. what is the current date in the dataset
* **version** - Report version. If not present means they were run with verion 1. See Methods page for more details.
