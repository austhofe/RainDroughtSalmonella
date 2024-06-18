# Southwest Climate Change and Enteric Diseases

#### A research compendium for exploring the effect of precipitation and drought on _Salmonella_ and _Campylobacter_ in the 4 corners states
**Under Review with EHP:** Association between precipitation events, drought, and animal operations with _Campylobacter_ infections in the Southwest US, 2009–2021
**Under Review with One Health:** Association between precipitation events, drought, and animal operations with _Salmonella_ infections in the Southwest US, 2009–2021
 

[Report Bug](https://github.com/austhofe/4CornersCCandFBD/issues) · [Request Feature](https://github.com/austhofe/4CornersCCandFBD/issues) · [Contribute](https://github.com/austhofe/4CornersCCandFBD/pulls)

## About The Project

This is a GitHub repository for a research project that explores the association between precipitation, drought, and presence and density of livestock on human enteric illness in Arizona, Colorado, New Mexico, and Utah. All data, except human case data, are available via this compendium. Instructions for collecting data, as well as code for merging and linking data are available to help others reproduce the results and conduct this work in other areas. Although surveillance data in this analysis are not considered protected health information, health data require a data use agreement with each individual state health department in order to gain access. Please contact the lead author for further guidance: Erika Austhof, [barrette\@arizona.edu](mailto:barrette@arizona.edu)

## Getting Started

To get started using any data or code, click on the folder and file you want. Click on the Copy button in order to copy and paste it into your own code line, or clone the repository to your own GitHub to get access to the full project.

### Data Sources
Data Sources used in this analysis
    - [PRISM](https://prism.oregonstate.edu/explorer/), meteorological data daily and 30-year normals by county-level centroid
    
    - [NOAA](https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/county/time-series), drought severity county time series
    
    - [NOAA](https://www.ncei.noaa.gov/access/monitoring/enso/soi), NCEI Southern Oscillation Index
    
    - [USDM](https://droughtmonitor.unl.edu/dmData/Timeseries.aspx), drought severity time series
    
    - [USDA Animal Census](https://www.nass.usda.gov/Data_and_Statistics/County_Data_Files/Livestock_County_Estimates/index.php), presence and density data
    
    - Köppen-Geiger climate zone, sensitivity analysis
        - Beck HE, Zimmermann NE, McVicar TR, Vergopolan N, Berg A, Wood EF. Present and future Köppen-Geiger climate classification maps at 1-km resolution. Sci Data. 2018;5(1):180214. doi:10.1038/sdata.2018.214
        
    - [US Census](https://www.census.gov/geographies/reference-files/time-series/geo/gazetteer-files.html), land area by county
    
    - [US Census](https://www.census.gov/data/datasets/time-series/demo/popest/2010s-counties-total.html), 2010 population estimates
    
    - [US Census](https://www.census.gov/data/datasets/time-series/demo/popest/2020s-counties-total.html), 2020 population estimates

### Steps for Linking and Merging Data

1.  Merge PRISM daily weather by county with surveillance data by report date and county

    -   If health data is a line list, aggregate counts of cases by report date

    -   Create one data frame that merges in all county-level weather and health data so you have a time series data frame for the time period in the state

    -   Extract year, month, week of year, and day from date field for future merging steps

    -   Merge in 30 year normal data by month and county in order to 

2.  Create an Excel sheet with county-level information including at a minimum: county name, FIPS, Climate Division, PRISM latitude, longitude, and elevation

3.  Merge county-level information with weather and health data frame by county

4.  Merge in social vulnerability data from CDC by county and year

    -   Create a SoVI average for 2010 by aggegrating R_PL_Themes by county (FIPS)

    -   Keep only FIPS, PRL_Themes, and year from SoVI datasets

    -   Assign SoVI to missing years by carrying forward data

5.  Merge in urban vs. rural designation from the US Census by county

6.  Merge in drought data by climate division and month

7.  Create variables for analysis

    -   Extreme Precipitation: Compare the daily precipitation to monthly and county-level 30 year normals. If daily value is above 30 year normals, then it was an extreme precipitation event.

    -   Drought: Using each drought index, create a presence/absence variable for drought. This should be a binary value, for example if PDSI is positive, assign a value of 0, if it's negative, assign a value of 1. Categorize PDSI into drought severity level.

    -   ENSO Years: Assign a designation for ENSO years for years: 2006--07, 2009--10, 2014--16, and 2018--19. The latest ENSO years are available from the [NWS Climate Prediction Center](https://origin.cpc.ncep.noaa.gov/products/analysis_monitoring/ensostuff/ONI_v5.php)
<<<<<<< HEAD
=======

    -   *Rainy Season: Identify each state's rainy season and create a variable that identifies which months in each year are generally considered rainy.*
>>>>>>> b7061c73407662125291f47c82989f619a632a3f

8.  *Aggregate daily data to different timescales and export. In the end, you should have 3 separate data frames for daily, weekly, monthly weather.*
9.  *Create seperate datasets or variables for sensitivity analyses*
    -  *Confirmed cases only*
    -  *A variable for COVID years, potentially restricting before 2019.*

## Usage and Resources

This project is set up so that you can follow the same protocol that we did in your own work, with easy to follow screenshots, commented code, and additional resources for collecting data in your own jurisdiction.

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this project better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement". Don't forget to give the project a star! Thanks again!

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## License

Distributed under the GNU 3.0 License. See `LICENSE.txt` for more information.

## Contact

Erika Austhof - [\@epierika](https://twitter.com/epierika) - [barrette\@arizona.edu](mailto:barrette@arizona.edu)

Project Link: <https://github.com/austhofe/4CornersCCandFBD>
