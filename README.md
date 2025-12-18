# ATMS-523-Final-Project-Module-8 
### Author: Domenic Brooks
### This is the repository for ATMS 523 final project. 

## Objective
My objective with this project was to garner a better understanding for which climate teleconnection indices are most impactful when it comes to monthly winter snowfall by building a ML model that can predict monthly snowfall anomalies. My motivation stems from my desire to better understand the complex interactions between teleconnections and winter snowfall on a sub-seasonal to seasonal scale for my home city, Baltimore, MD. 

## Methodology
The dataset I used for snowfall is the ERA-5 reanalysis dataset, specifically the ARCO-ERA5 dataset (see documentation below). For the climate teleconnections, I used datasets from NOAA NCEI and CPC to get monthly indices for the ENSO, PDO, IOD, AO, NAO, and PNA, which were the primary teleconnections used in this analysis. I conducted a 1-month lagged correlation to see which month had the most snowfall predictability, and from there conducted a series of tests with various ML modeling techniques to see which teleconnections had the greatest influence on monthly snowfall.
All the data processing, analysis, and conclusions can be found in the `data_preprocessing.ipynb` notebook in this repository.


## Data Source (Teleconnections)
##### For ENSO, PDO, and IOD: https://www.ncei.noaa.gov/pub/data/cmb/ersst/v5/index/
##### For AO, NAO, and PNA: https://www.cpc.ncep.noaa.gov/products/precip/CWlink/daily_ao_index/teleconnections.shtml 

## Data Source (ARCO-ERA5)
Carver, Robert W, and Merose, Alex. (2023):
ARCO-ERA5: An Analysis-Ready Cloud-Optimized Reanalysis Dataset.
22nd Conf. on AI for Env. Science, Denver, CO, Amer. Meteo. Soc, 4A.1, https://ams.confex.com/ams/103ANNUAL/meetingapp.cgi/Paper/415842

See documentation: https://github.com/google-research/arco-era5 

## ERA-5 Dataset
Hersbach, H., Bell, B., Berrisford, P., Hirahara, S., Horányi, A., 
Muñoz‐Sabater, J., Nicolas, J., Peubey, C., Radu, R., Schepers, D., 
Simmons, A., Soci, C., Abdalla, S., Abellan, X., Balsamo, G., 
Bechtold, P., Biavati, G., Bidlot, J., Bonavita, M., De Chiara, G., 
Dahlgren, P., Dee, D., Diamantakis, M., Dragani, R., Flemming, J., 
Forbes, R., Fuentes, M., Geer, A., Haimberger, L., Healy, S., 
Hogan, R.J., Hólm, E., Janisková, M., Keeley, S., Laloyaux, P., 
Lopez, P., Lupu, C., Radnoti, G., de Rosnay, P., Rozum, I., Vamborg, F.,
Villaume, S., Thépaut, J-N. (2017): Complete ERA5: Fifth generation of 
ECMWF atmospheric reanalyses of the global climate. Copernicus Climate 
Change Service (C3S) Data Store (CDS). (Accessed on 17-12-2025)
DOI: 10.24381/cds.143582cf 

Hersbach et al, (2017) was downloaded from the Copernicus Climate Change 
Service (C3S) Climate Data Store. We thank C3S for allowing us to 
redistribute the data.

The results contain modified Copernicus Climate Change Service 
information 2022. Neither the European Commission nor ECMWF is 
responsible for any use that may be made of the Copernicus information 
or data it contains.
