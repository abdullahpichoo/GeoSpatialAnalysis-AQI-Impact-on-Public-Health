# Spatial Data Science Project

This project aims to explore the relationship between air quality and the incidence of influenza-like illnesses (ILI) in the United States. The project uses spatial data analysis techniques to visualize the air quality index of US Counties on shapefiles, and overlay the number of ILI cases on top of the air quality data to identify potential correlations.

## Project Title

The project is titled "Impact of Air Quality on Influenza Like Illnesses".

## Datasets

The project uses three datasets, which are:

#### USA Counties Dataset:

This dataset contains the geometries of all the US counties. This dataset will be used to plot the results on a map. The dataset details are as follows:
Column Names:

- NAME: Name of the county
- STATE_NAME: Name of the state where the county is located
- geometry: geometry of the county

#### Air Quality Index Dataset:

This dataset includes the daily air quality index of US counties. This dataset will be used to visualize the air quality index of US counties on shapefiles. The dataset details are as follows:
Column Names:

- State Name: The name of the state in which the county is located.
- County Name: The name of the county for which the AQI is measured.
- State Code: The two-letter code for the state in which the county is located.
- County Code: The three-digit code for the county.
- Date: The date on which the AQI was measured.
- AQI: The Air Quality Index value for the given county and date. AQI is a measure of how clean or polluted the air is and what associated health effects might be a concern for that day.
- Category: The corresponding AQI category based on the AQI value. AQI categories range from "Good" (0-50 AQI) to "Hazardous" (301-500 AQI).
- Defining Parameter: The pollutant that has the highest contribution to the AQI on the given day.
- Defining Site: The site from which the AQI was measured.
- Number of Sites Reporting: The number of sites reporting the AQI for the given county and date.

#### Illness Cases Dataset:

This dataset includes the weekly number of cases of influenza-like diseases. This dataset will be used to overlay the number of ILI cases on top of the air quality data to identify potential correlations.The dataset details are as follows:
Column Names:

- season: This column counts the year in terms of seasons i.e. 2017-2018 is one season.
- date_code: Centers for Disease Control and Prevention (CDC) Morbidity and Mortality Report (MMWR) Week. Format is YYYYWW. Weeks begin on Sunday and end on Saturday.
- weekending: Date of the last day included in the CDC MMWR Week (Saturday). Format MM/DD/YYYY.
- region: Names of region where data was collected. Regions are written as multiple counties for example "Central" includes Calaveras, Fresno, Inyo, Kings, Madera, Mariposa, Merced, Mono, Monterey, San Benito, San Joaquin, Stanislaus, Tulare, and Tuolumne counties.
- Influenza_Category: Total number of specimens positive for influenza, all types
- Count: Number of specimens meeting the criteria listed in the Influenza_Category field

## Methodology

The project uses spatial data analysis techniques to visualize the air quality index of US counties on shapefiles, and overlay the number of ILI cases on top of the air quality data to identify potential correlations. The following steps were taken:

- Load the USA Counties Dataset and the Air Quality Index Dataset.

- Merge the two datasets based on the county name to create a new dataset that includes the air quality index data for each county.

- Load the Illness Cases Dataset.

- Merge the new dataset from step 2 with the Illness Cases Dataset based on the county name to create a final dataset that includes the air quality index and the number of ILI cases for each county.

- Visualize the air quality index of US counties on shapefiles using a chloropleth.

- Overlay the number of ILI cases on top of the air quality data to identify potential correlations.

## Results

As we can see from these results, there is no corelation between the data of Influenza Cases and AQI data. The reasons can the following:

- The influenza cases does not represent the level of illness caused by poor air quality.
- The influenza cases data was high resolution and was available region wise whereas the AQI data was available county wise. AQI is different for every county and a cluster of counties does not correctly respresent its overall air quality.
