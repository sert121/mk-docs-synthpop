## Preprocessing

### 6. Filtering the IHDS data


```python
# state and district id can be found out using census metadata
import pandas as pd
ihds_individuals_data = pd.read_csv(ihds_individuals_filename, sep='\t')

filtered_ihds_individuals_data = ihds_individuals_data.loc[ihds_individuals_data.STATEID==state_id]

filtered_ihds_individuals_data = filtered_ihds_individuals_data[filtered_ihds_individuals_data['DISTID'].apply(lambda x : x in district_ids)]

ihds_households_data = pd.read_csv(ihds_household_filename, sep='\t')

filtered_ihds_households_data = ihds_households_data.loc[ihds_households_data.STATEID==state_id] 

filtered_ihds_households_data = filtered_ihds_households_data[filtered_ihds_households_data['DISTID'].apply(lambda x : x in district_ids)]
#Reading and filtering survey sample data
```