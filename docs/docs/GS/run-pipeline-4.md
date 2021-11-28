### 8. Adding additional features to the base population

- Adding Household coordinates (latitude,longitude) to the base population

```python
# admin_units_geojson_filename, admin_units_population_filename, population_density_filename have been defined in the first step (LoadData)

hlat_hlong_age_object = HLatHlongAgeAddition(admin_units_geojson_filename, admin_units_population_filename, population_density_filename)

hlat_hlong_age_object.admin_units['WARD']= hlat_hlong_age_object.admin_units['WARD'].astype(int)

# perform_transforms() returns the modified base population
new_synthetic_population = hlat_hlong_age_object.perform_transforms(synthetic_individuals, synthetic_households)

```

- Adding age, height ,weight attributes to the base population
```python
#loading dta IHDS data
path_to_ihds_data_DTA = "path_to_IHDS_data[DTA format]"

# adding height weight and age
new_synthetic_population = age_height_weight(output_file_name,path_to_ihds_data_DTA)

```
Source to Current IHDS_DTA_data [here](https://drive.google.com/file/d/1ho90BysemsVKsyrh-XuSlvEBAw2w_KCY/view?usp=sharing) 
You can find more details about the IHDS data format [here](https://www.icpsr.umich.edu/web/DSDR/studies/36151)