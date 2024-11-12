# Southwest Climate Change and Enteric Diseases

#### A research compendium for exploring the effect of precipitation and drought on _Salmonella_ infections in the 4 corners states

**Under Review with One Health:** Association between precipitation events, drought, and animal operations with _Salmonella_ infections in the Southwest US, 2009–2021
 

[Report Bug](https://github.com/austhofe/4CornersCCandFBD/issues) · [Request Feature](https://github.com/austhofe/4CornersCCandFBD/issues) · [Contribute](https://github.com/austhofe/4CornersCCandFBD/pulls)

## About The Project

Using public health surveillance, meteorological, and farm animal census data from Arizona, Colorado, New Mexico, and counties in Utah, this ecological study aims to assess the association between precipitation and the incidence of Salmonella infections by county from 2009–2021 and determine how this association is modified by prior drought level and animal operations. We merged 29,350 cases of salmonellosis reported in 127/141 counties with total precipitation (inches), temperature (average °F), Palmer Drought Severity Index (PDSI, category), and animal census data (density per square mile) by week from 2009–2021. Negative binomial generalized estimating equations adjusted for temperature with a 2-week lag were used to explore the acute association between precipitation and salmonellosis with resulting Incidence Rate Ratios (IRR). We then conducted stratified analyses to explore the association with precipitation following antecedent drought level and type of animal density (per square mile) on this association. 

## Getting Started

This is a GitHub repository for a research project that explores the association between precipitation, drought, and presence and density of livestock on human enteric illness in Arizona, Colorado, New Mexico, and Utah. All data, except human case data, are available via this compendium. Instructions for collecting data, as well as code for merging and linking data are available to help others reproduce the results and conduct this work in other areas. Although surveillance data in this analysis are not considered protected health information, health data require a data use agreement with each individual state health department in order to gain access. Please contact the lead author for further guidance: Erika Austhof, [barrette\@arizona.edu](mailto:barrette@arizona.edu)

To get started using any data or code, click on the folder and file you want. Click on the Copy button in order to copy and paste it into your own code line, or clone the repository to your own GitHub to get access to the full project.

### Data Sources
Data Sources used in this analysis

•	[PRISM](https://prism.oregonstate.edu/explorer/), meteorological data daily and 30-year normals by county-level centroid 

•	[NOAA](https://www.ncei.noaa.gov/access/monitoring/climate-at-a-glance/county/time-series), drought severity county time series

•	[NOAA](https://www.ncei.noaa.gov/access/monitoring/enso/soi), NCEI Southern Oscillation Index

•	[USDM](https://droughtmonitor.unl.edu/dmData/Timeseries.aspx), drought severity time series

•	[USDA Animal Census](https://www.nass.usda.gov/Data_and_Statistics/County_Data_Files/Livestock_County_Estimates/index.php), presence and density data

•	Köppen-Geiger climate zone, sensitivity analysis
        - Beck HE, Zimmermann NE, McVicar TR, Vergopolan N, Berg A, Wood EF. Present and future Köppen-Geiger climate classification maps at 1-km resolution. Sci Data. 2018;5(1):180214. doi:10.1038/sdata.2018.214
        
•	[US Census](https://www.census.gov/geographies/reference-files/time-series/geo/gazetteer-files.html), land area by county

•	[US Census](https://www.census.gov/data/datasets/time-series/demo/popest/2010s-counties-total.html), 2010 population estimates

•	[US Census](https://www.census.gov/data/datasets/time-series/demo/popest/2020s-counties-total.html), 2020 population estimates


## Usage and Resources

This project is set up so that you can follow the same protocol that we did in your own work, with data sources, R and Stata code, and additional resources for merging data with data in your own jurisdiction.

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

Erika Austhof - [barrette\@arizona.edu](mailto:barrette@arizona.edu)

Project Link: <https://github.com/austhofe/4CornersCCandFBD>
