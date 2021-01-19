## Data Schema

* **date** - ISO Date for the predicted number of infection/deaths/hospital burden
* **compartment** - One of deaths, infections, hospital demand and ICU demand or Rt, Reff. Cumulatives are also given as well as prevalence - which is all active infections, which includes hospitilised and non-hopsitilised cases
* **y_025, y_25, y_median, y_mean, y_75, y_975** - Summary statistics for the compartment. E.g. y_25 is the 25% quantile
* **scenario** - The intervention scenario explored. One of Maintain Status Quo, Additional 50% Reduction, Relax Interventions 50%. Surged Maintain Status Quo also present in countries estimated to pass capacity in next 28 days.
* **country** - Country name
* **iso3c** - Country ISO3C letter
* **report_date** - ISO Date at which the reports were generated, i.e. what is the current date in the dataset
* **version** - Report version. If not present means they were run with verion 1. See Methods page for more details.
* **death_calibrated** - Scenario calibrated to death data. In countries with no deaths to date, we provide scenario projections of what would happen if 5 imported cases occurred today with no future intervention changes. We assume three different R0s. For our upper estimate, we assume that R0 is equal to the mean R0 of countries in the same income classifcation (High, Upper Middle, Lower Middle, Low Income). For our lower estimate, we assume that R0 is equal to either 1.2 or the current Rt of countries in the same income classifcation (whichever is highest). Lastly, our central estimate is half way between the upper and lower estimate. These 3 scenarios are labelled as Relax Interventions 50%, Additional 50% Reduction and Maintain Status Quo in order to maintain consistency with the calibrated scenarios.
