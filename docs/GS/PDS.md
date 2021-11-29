
## Population Density Sampling

`population_density_sampler.py` houses the following functions for population density sampling.  
```python
class PopulationDensitySampler:
    def __init__(self, population_density_filename:str) :
```
> This class is used to sample the population density from the population density file.

> - Loads the population density file

```python
class PopulationDensitySampler:
    def add_point(self, latitude:float, longitude:float) :
```
> - Adds new points to the population density file

```python
class PopulationDensitySampler:
    def get_lat_long_samples(self, n, polygon) :
```
> - Samples points from a given polygon file in accordance to the population density



