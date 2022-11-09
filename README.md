# Southwest Climate Change and Enteric Diseases

#### A research compendium for exploring the effect of precipitation and drought on Salmonella and Campylobacter in the 4 corners states

[Report Bug](https://github.com/austhofe/4CornersCCandFBD/issues) · [Request Feature](https://github.com/austhofe/4CornersCCandFBD/issues) · [Contribute](https://github.com/austhofe/4CornersCCandFBD/pulls)

## About The Project

This is a GitHub repository for a research project that explores the association between precipitation, drought, and temperature on human enteric illness in the 4 corners states. This is a collaboration between Arizona, Colorado, New Mexico, and Utah.

## Getting Started

To get started using any data or code, click on the folder and file you want. Click on the Copy button in order to copy and paste it into your own code line, or clone the repository to your own GitHub to get access to the full project.

### Steps for Linking and Merging Data

1.  Merge PRISM daily weather by county with surveillance data by report date and county

    -   If health data is a line list, aggregate counts of cases by report date

    -   Create one data frame that merges in all county-level weather and health data so you have a time series data frame for the time period in the state

    -   Extract year, month, week of year, and day from date field for future merging steps

    -   Merge in 30 year normal data by month and county

2.  Create an Excel sheet with county-level information including at a minimum: county name, FIPS, Climate Division, PRISM latitude, longitude, and elevation

3.  Merge county-level information with weather and health data frame by county

4.  Merge in social vulnerability data from CDC by county and year

    -   Create a SoVI average for 2010 by aggegrating R_PL_Themes by county (FIPS)

    -   Keep only FIPS, PRL_Themes, and year from SoVI datasets

    -   Assign SoVI to missing years by carrying forward data

5.  Merge in urban vs. rural designation from the US Census by county

6.  Merge in drought data by climate division and month

7.  *Create variables for analysis*

    -   *Extreme Precipitation: Compare the daily precipitation to monthly and county-level 30 year normals. If daily value is above 30 year normals, then it was an extreme precipitation event.*

    -   *Drought: Using each drought index, create a presence/absence variable for drought. This should be a binary value, for example if PDSI is positive, assign a value of 0, if it's negative, assign a value of 1.*

    -   ENSO Years: Assign a designation for ENSO years for years: 2006--07, 2009--10, 2014--16, and 2018--19. The latest ENSO years are available from the [NWS Climate Prediction Center](https://origin.cpc.ncep.noaa.gov/products/analysis_monitoring/ensostuff/ONI_v5.php)

8.  *Aggregate daily data to different timescales and export. In the end, you should have 4 separate data frames for daily, weekly, monthly, and seasonal weather.*

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
