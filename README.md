# AFS Standard Fish Data App

The primary purpose of this application is to display data collected across North America on fish species, using a standardized collection approach and resulting comparable metrics by AFS. Additionally, users can upload their own data to compare to the provided standardized data.

### Repository file organization

**Dashboard**

-   `app/app.R`: file that generates dashboard showing standardized fish data and allows user to upload data to compare
-   `app/Test_results_full_012723.csv`: standardized fish data file
-   `app/R/functions.R`: functions to calculate three metrics of interest
-   `app/www/AFS_sponsor_3.png`: image file with sponsor logo displayed on dashboard "About" page

**Data prep**

-   `app/process_user_data.Rmd`: generates example user upload data (`user_example.csv`) shown in app; shows development of metric calculations
-   `app/user_example.csv`: example user upload data
-   `app/download_map_data.R`: code to download the [EPA Ecoregions](https://www.epa.gov/eco-research/ecoregions) data used in app map
-   `analysis_scripts`: folder with scripts to prepare standardized data; newer version of this is in `app/R/functions.R`
-   `input_examples`: folder containing additional user upload example datasets

**Package versions & dependences**

-   `renv` folder
-   `renv.lock`
-   `.Rprofile`

**Repository metadata**

-   `.gitignore`
-   `AFS_database_code.Rproj`
-   `LICENSE`
-   `README.md`
-   `CITATION.cff`

### How to cite

Please use the citation below if you use or modify this tool for research purposes.

### How to contribute

If you would like to suggest or make changes to this app, there are a few ways to do so. You can reach out via email to [Scott Bonar](mailto:SBonar@ag.arizona.edu) or the [CCT Data Science team](mailto:cct-datascience@arizona.edu) with suggestions.You can also create an issue describing a problem with the code or improvements. Because this is a forked repo, issues need to be made in the [upstream repo](https://github.com/erinetracy/AFS_database_code) under the "Issues" tab.

If you can make changes to the code yourself, feel free to fork this repo and make a pull request. To run the code locally, it is necessary to download the ecoregions map data by running `app/download_map_data.R` and have access to the standardized fish records location data file `app/Lat_long_AFSshiny_012023.csv`. Package versions and dependencies are tracked with `renv`.
