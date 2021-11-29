### 10. [Optional] Additional Attributes - Jobs  
`under progress`


### 11. [Optional] Additional Attributes - Places
The Places class helps us assign workplaces, schools and public places.
```python
# from places.py import Places class
from places import Places
places_object = Places(1, len(synthetic_population), n_processes)
synthetic_population.drop(synthetic_population.columns[0], axis=1, inplace=True)
synthetic_population.drop(synthetic_population.columns[0], axis=1, inplace=True)
synthetic_population

places_object.generate_workplaces(list(synthetic_population["JobLabel"]))
places_object.generate_schools()
places_object.generate_public_places()

adults = synthetic_population[synthetic_population["age"] > 18]
adults = places_object.assign_workplaces(adults)

children = synthetic_population[synthetic_population["age"] < 19]
children = places_object.assign_schools(children)

total_population = pd.concat([adults, children], axis=0)
total_population = places_object.assign_public_places(total_population)
```