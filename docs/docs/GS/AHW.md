### Adding  Age, Height, Weight attributes to the synthetic dataset
`age_height_weight.py` helps us add age, height, and weight to the synthetic dataset. It has the following functions.  

```python
def load_data(synthetic_pop:str,ihds:str) -> Tuple[DataFrame,DataFrame]:
```
> Loads the IHDS and synthetic population data.

```python
def modify_age_gender(synthetic_population:DataFrame) -> DataFrame: 
```
> Adds age and gender labels in accordance to the values

```python
def renaming_columns(ihds_df:DataFrame) -> DataFrame:
```
> Selects a subset of relevant colums, and maps them to a better naming convetion
```python
def boundary_df(ihds_df:DataFrame, district:str) -> Tuple(DataFrame,DataFrame):
```
> Create a boundary dataframe according to district,sex

```python
def assign_height_weight(df:DataFrame, sex:str, parameter:str):
```
> Assign height and weight to individuals in proportion to age and gender