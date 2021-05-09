## Project 1: Home Value Patterns Due to COVID-19

By: Jason Sheridan, Anna Sours, Jenni Davis, Austin Olea, & Mark Blankenship


### Hypothesis: Where COVID-19 cases are higher in counties with major cities, home values will increase in the surrounding counties.

#### Guiding Questions:
* How are people migrating throughout the US since COVID 19 began?
* Has this impacted home values? 
* Is there a relationship between cases and the housing market? 

### Data Sources:
#### COVID-19 Cases: 
* NY Times US states & counties
* Texts files with state, county, date, cases, etc. 
* US census data
  * Shapefiles 
* API calls
  * Coordinates
* New dependencies for mapping
  * geopandas
  * folium 

#### Home values:
* Zillow Home Value Index (ZHVI) from zillow.com
  * CSV files updated monthly
  * ZHVI values for Metro & U.S. 
  * Monthly values from 1/31/1996 - 12/31/2020

### COVID-19 Data Exploration
#### Analysis 1: 
##### NY Times US states & counties
  * Q: What states have the highest count of COVID-19 cases? And of those states, which counties had the highest  count of COVID-19 cases? 


##### Exploration & Data Wrangling: 
* NY Times data
  *US states & counties data - date, state, county, cases, etc.

    * Methods: 
      * Filtering
      * Grouping
      * Stats
      * Dropping values
      * Sorting values
      * Horizontal bar chart

#### Analysis 2: 
##### API calls, US census data & geopandas
  * Q: Can we take the NYTimes data and layer it onto a map of the United States and have it display state name and maximum case counts?

##### Exploration & Data Wrangling: 
* API calls
  *Coordinates
* US census data
  *Shapefiles 
*  Geopandas


  * Methods: 
    * API calls 
    * Shapefiles
    * Export/Import csv files
    * More: filtering, grouping, dropping
    * Adding/renaming columns
    * Merging

![USmapColorbar.png](Image/USmapColorbar.png?raw=true "Title")

* States determined for further analysis:
  * California
  * Texas
  * Florida
  
  
#### Analysis 3: 
##### More mapping…?
  * Q: Can we use heat maps and markers to better highlight the counties with maximum cases and their surrounding counties?

##### Exploration & Data Wrangling: 
* Folium
  * Mapping library 

  * Methods: 
    * Gmaps 
    * Heatmaps
    * Folium
    * Lists...
    * Lists of coordinates...
    * Lists of cities...
    * LISTS!

### Home Values of Counties with high COVID-19 Cases
#### California
![tri_county_zhvi.png](output/tri_county_zhvi.png?raw=true "Title")

#### Florida
![highest_covid_counties_fl.png](output_data/highest_covid_counties_fl.png?raw=true "Title")

#### Texas
![county_lines.png](county_lines.png?raw=true "Title")

### Percent Change in Home Values 
* The blue bars show the average home value increase over the 3 years prior to covid.
 * pre_covid_annual=((((feb2020-mar2017)/feb2020)/3)*100).values[0]
 
* The orange bars show the home value increase from March 2020, when the covid lockdowns began until December 2020.
  * covid_annual=(((dec2020-mar2020)/dec2020)*100).values[0]
  
 Comparing the home values of the pre-Covid and during Covid time frames for the counties with the highest number of covid cases as well as the surrounding counties, most of the surrounging counties did see a greater percentage increase in home values after the Covid lockdowns began than in the years before Covid.
 
#### California
![los_angles_metro.png](output_data/los_angles_metro.png?raw=true "Title")

#### Florida
![miami_metro_county.png](output_data/miami_metro_county.png?raw=true "Title")

#### Texas
![dfwmetro2.png](dfwmetro2.png?raw=true "Title")

![houstonmetro2.png](houstonmetro2.png?raw=true "Title")

#### Conclusion Summary
* In the majority of the metro-area counties analyzed, home values increased at a greater rate in 2020 than the average rate from 2017-2019. It also appears that values increased at a proportionally higher level in areas with lower COVID-19 cases.

#### Implications of findings
* What does our conclusion mean?
  * According to these metrics, in most areas, we found increased home values in counties surrounding cities with highest  COVID-19 cases. This  could be due to a    desire to leave more densely populated areas, away from areas with higher COVID cases.
* What are next steps/further analysis? 
  * Analyze data from counties with major cities with fewer COVID-19 cases
  * Analyze housing values against other market factors to further understand the impact of COVID-19
  * Analyze type and size of home purchased against the type of home sold by a particular buyer

  
