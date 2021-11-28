# Configuration


## Setting the Data sources
Synthpop uses data from different sources to generate the synthetic population.  
The data sources are:  

- IHDS Human survey data, 2011
    - [[Source]]("https://www.icpsr.umich.edu/web/DSDR/studies/36151")
    - [[Download]]("https://drive.google.com/file/d/1zAKK2i6vpJjmWkSzK_AF0GA-e26lmaYl/view?usp=sharing")
- Census Survey of India
    - [[Source]]("https://censusindia.gov.in/2011-common/censusdata2011.html")
    - [[Download]]("")


## Preprocessing the Data
`coming soon`


## Installing the requirements

`pip install -r requirements.txt` to install the required dependencies for the project.

Once you're set, you should be able to see the following files:
- synthpop.py : Starter file
- IPU.py : IPU(Iterative Proportional Updating) algorithm
- age-height-weight.py : Adding age/height attributes on the base-population
- HlatHlongaddition.py : Adding household attributes on the base-population 
- places.py : Adding places attributes on the base-population
- population_density_sampler.py : Helper file for sampling the population
