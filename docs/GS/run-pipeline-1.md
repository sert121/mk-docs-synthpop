



### 1. Loading the data from IHDS and Census survey of India
```python
householdh_marginal_filename = "path_to_household_marginals"
individuals_marginal_filename = "path_to_individual_marginals"

ihds_individuals_filename = "path_to/36151-0001-Data.tsv"
ihds_household_filename = "path_to/36151-0002-Data.tsv"
```

### 2. Geojson Spatial Data 

Setting the data sources for geojson spatial data for wards.  
Current source: [[Municipal Spatial Data]](https://github.com/datameet/Municipal_Spatial_Data)      
This Repository will contain the spatial data of all the  Municipalities that has been scraped from their websites and other sources. Do note, that the wards in these datasets, are usually the Municipal wards, and not the Census wards.
Geojson ward names should match with the ward names in the `ward-wise population` file (See Next Steps), so that one can use it as a primary key. If they don't match please rename them accordingly.For example if the ward name in geojson is `Ward-1` and in population file is `Ward 1`, then rename it to `Ward-1` in the population file.

```python 
# Example geojson using Kolkata as the city
admin_units_geojson_filename = "https://raw.githubusercontent.com/datameet/Municipal_Spatial_Data/master/Kolkata/kolkata.geojson"
```

### 3. Loading the Population Density Data
Current source for population density data: [[Link]](https://data.worldpop.org/GIS/Population_Density/Global_2000_2020_1km/2020/IND/ind_pd_2020_1km_ASCII_XYZ.zip) [Note: Please unzip to access the `.csv` file]
```python
population_density_filename = "/path_to/ind_pd_2020_1km_ASCII_XYZ.csv"
```

### 4. Loading ward wise population

```python
admin_units_population_filename="path_to_file"
#after loading the data, one can specify the total population of each ward using column name TOT_P in their respective datadrames
```
Current Source for ward-wise population: [CensusGov](https://censusindia.gov.in/pca/pcadata/pca.html)

To get ward wise lat-long, one can use either of the following sources:
 
`https://github.com/geopy/geopy`  
`https://www.mapmyindia.com/api`  
`https://developers.google.com/maps/documentation/geocoding/overview`  

Next we would  merge the ward-wise population with the lat-long data *(keeping Ward Name/no. as the unique key)*   

**Sample Format**: 

|Ward| Latitude | Longitude | TOT_P 
|---|---|---|---|  
|Kolkata Ward 2|88.34| 83.34| 111000  
|Kolkata Ward 3|85.33| 89.77| 99991 


### 5. Setting the state and district ID
State and district ID can be found out using Census MetaData found [[here]]("https://censusindia.gov.in/2011census/Listofvillagesandtowns.aspx").

```python
# select state id
state_id = 19 # West Bengal

#Select distid within state
district_ids = [17] # Kolkata
```

