## IPU

### 7. Generating the base population using Iterative Proportional Updating (IPU)

```python
###IPU Step
from IPU import IPU
ipu_object = IPU()

#passing all requirements to the IPU function
synthetic_households, synthetic_individuals, synthetic_stats = ipu_object.generate_data(filtered_ihds_individuals_data, filtered_ihds_households_data, householdh_marginal_filename, individuals_marginal_filename)
###IPU Step
```