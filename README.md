# Food Deserts and Birth Outcomes
#### NYU CUSP ML for cities class, Spring 2018,
Prof. Daniel Neil

Project by Rebecca Scheidegger, Emily Padvorac, Dana Chermesh

- _[Full report](!ADD!)_
- _[Presentation](https://github.com/danachermesh/Food_Deserts_ML/blob/master/FoodDesertBirthOutcomes_MLforCities2018.pdf)_

## Objective
This research aims to identify the important factors impacting low birthweight and preterm births on the zip code level, using random forests and Bayesian network approaches. Identifying if  certain variables are important in determining negative birth outcomes can help decide what policy levers to pull or what demographic groups to focus intervention programs on. These findings are applicable to New York government at both the state and local level, and would be most relevant to the Department of Health. Additionally, the research is applicable to hospitals or healthcare providers who can help identify at-risk persons. This research seeks to understand to what extent living in a food desert may have on birth outcomes. In recent years, the topic of food deserts has become increasingly popular. In short, a food desert is an area that has low-access to healthy, nutritious food.


## Data
_Data that were in used can be found in this GitHub repo under [data folder](https://github.com/danachermesh/Food_Deserts_ML/tree/master/data)_

_Birth Outcome Variables Data_
Two adverse birth outcomes were considered: preterm birth and low birthweight. Data on these outcomes were collected from New York State Department of Health at the zip code level.

_Population Variables Data_
At the beginning of research, a dataset containing variables on food deserts was considered. However, the variables had extremely high multicollinearity. As such, data was gathered on a subset of the variables most relevant to the aim of the research. Data was collected and derived from the **American Community Survey (ACS) 5-year (2009-2016)** at the zip code level. Variables included: 
  - **Citizenship status** 
  - **Poverty rate** 
  - **Health insurance coverage** 
  - **Vehicle Access**
  - **SNAP (Food Stamp) Benefits**
A variable of **teen birth rate** was also considered, and was retrieved from the NYS Department of Health data. Additionally, each zip code was classified as either urban or rural, using classifications as defined by the US Census Bureau.

_Data limitations_
- **Mother’s age**: The age of the mother is a known factor related to negative birth outcomes. In particular, women under 18 or over 35 are considered higher risk for preterm birth (National Institutes of Health).  However, data was not publically available on a zip code level for the age of mothers. Using teen birth rate as a variable is a partial proxy for this, although data was still not available for older mothers.

- **Multiple births**: Another factor that is known to increase the risk of adverse birth outcomes is multiple births (i.e twins) ((National Institutes of Health). Again, data was not publically available on a zip code level.  For this issue, it was assumed that multiple births occur at a similar rate in all areas.


## Methodology
_The complete analysis and the code used to generate it are found in this GitHub repo, seperated to the Ipython notebooks above_

All data that were included in this study are labeled, thus methodologies of _**supervised learning**_ only have been taken into consideration. <\br>
Two methodologies were used: _**random forest**_ and _**Bayesian network**_. Using two approaches allowed results to be compared and contrasted to better understand the structure and accuracy of model choice. 


## Results and Conclusions 
Overall, the random forest performed significantly better than the Bayesian networks for either birth outcome. Random forests are known to have higher accuracy. However, they are less interpretable. As discussed earlier, this can be a problem in the context of such a sensitive issue. 

In the random forest feature importance, uninsured percentages rank first for both preterm and low birthweight, following closely by food stamps percentages across the zip codes. The first rank makes sense as it can be assumed that uninsured women will conduct minimal, late, or no prenatal care at all, leaving them at higher risk for having pregnancy problems that will not be identified nor treated.

Having the food stamps ranked at the second highest importance suggests that food deserts do indeed matter in the context of adverse birth outcomes. Food stamps are only eligible to be used for certain products, and vitamins, such as prenatal vitamins, are not an allowed purchase (SNAP Website). Additionally, it has been  observed that food stamp recipients do not consume high-quality, nutritional food (Condon et al, 2015). Some potential policy proposals to be considered would be allowing the purchase of prenatal vitamins on food stamps or providing pregnant women with increased food stamp benefits during pregnancy so that they could access more nutritional food such as fresh fruits and vegetables, which tends to be more expensive. 

The third most important feature for both outcomes was poverty. There are obvious linkages between poverty, food stamps, and being uninsured. Overall, it is apparent that poverty rates and indicators of poverty (uninsured, food stamps) are extremely relevant to predicting negative birth outcomes. While poverty as a whole is a complex issue and difficult to address, it is constructive to know that individual factors such as being uninsured or being on food stamps have high importance in determining negative birth outcomes, as there are concrete and practical steps that can be taken to improve these programs for pregnant women, and therefore potentially reduce negative birth outcomes. 

## Limitation + future research
As mentioned, data on the age of mothers and the rate of multiple births was not available at the zip code. These conditions are medically known to result in adverse birth outcomes. Having these data would likely fine tune the results, by considering what percent of events was caused by these conditions. 

