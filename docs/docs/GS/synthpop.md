# Starter
 
> This covers the documentation for the `synthpop.py` file

## Description
```synthpop.py``` can be seen as the controller of the entire pipeline. It is responsible to chain the individual parts of the pipeline together.
It controls the flow of the data through the following steps:  

- Loading data  
- Preprocessing  
- IPU instance generation  
- Synthetic data generation  
- Feature addition  
- Data evaluation  
- Data export  

Each step is controlled by a separate file/module listed below:  

``` IPU.py ```  
``` population_density_sampler.py ```  
``` HlatHlongAddition.py ```  
``` places.py ```  
``` age_height_weight.py ```  
