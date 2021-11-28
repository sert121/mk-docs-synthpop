
# IPU : Iterative Proportional Updating

```python
class IPU:
    def preprocess_individual_samples_ihds(self,filtered_ihds_individual_samples : DataFrame ) -> DataFrame :
```
> This function preprocesses the individual samples of the raw IHDS data.

> - The attributes provided by IHDS_Survey are remapped to give clearer variable names to the attributes.
> - The ages are binned according to 10 year gaps (0-10, 10-20, 20-30, 30-40, 40-50, 50-60, 60-70, 70-80, 80-90, 90-100).
> - Each individual is assigned to a religion group based on the religion attribute.
> - Each individual is assigned to a particular Caste  based on the caste attribute.
> - Each individual is assigned a job-label on the basis of activity status

```python
class IPU:
    def preprocess_households_samples_ihds(self,filtered_ihds_households_data : DataFrame ) -> DataFrame :
```
> This function preprocesses the household samples of the raw IHDS data.  

> - The attributes provided by IHDS_Survey are remapped to give clearer variable names to the attributes.
> - Households are classified on the basis of rural/urban status.
> - Households are classified on the basis of household size.

```python
class IPU:
    def load_marginals(self,householdh_marginal_filename:str,
        individuals_marginal_filename:str,
        individuals_data:DataFrame,
        households_data:DataFrame) -> Tuple(DataFrame,DataFrame,list) :
```
> This function loads and preprocesses the households and individual marginals from the respective files.

```python
class IPU:
    def generate_data(self,householdh_marginal_filename:str,
        filtered_ihds_individuals_data: DataFrame,
        filtered_ihds_households_data: DataFrame,
        householdh_marginal_filename: str,
        individuals_marginal_filename: str) -> Tuple(DataFrame,DataFrame,DataFrame) :
```
> This function generates the synthetic population data from the marginal files and the ihds data.

