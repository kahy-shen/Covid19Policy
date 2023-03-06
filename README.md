# Quantifying COVID-19 policy impacts on subjective well-being during the early phase of the pandemic: A cross-sectional survey analysis

### Data Resource
---
We published the concatenated Gallup COVID-19 data and OxCGRT policy data in the Gallup+OxCGRT.csv file, including 9,285 data points. The data points can be used to figure out the partial correlation between three subjective well-being (SWB) variables and COVID-19 policy measures, build the fixed-effects regression, and conditional inference tree (CIT) model for SWB variables.

A sample code to run fixed-effects regression in Stats is:

```
xtreg Life_Satisfaction i.income	i.OldChild i.SmallChild	 i.job	i.gender	i.employ i.state	
		c.confirmed_x	c.deaths_x	i.school_closing_x	c.demo_age	i.demo_marital_status_2017 
		c.NoChildren, fe
```

A sample code to create the conditional inference tree in R is:

```
ConInfTree <- ctree(Lifeindex ~ Income + OldChild + SmallChild + Job + Gender + Employ + Confirmed 
				+ Deaths + School_closing + Workplace_closing + Cancel_events + 
				+ Gatherings_restrictions + Transport_closing + Stay_home_restrictions + 
				+ Internal_movement_restrictions + Testing_policy + Contact_tracing + Age + 
				+ Marital.status + No..children, 
				data = data,  control=ctree_control( alpha = 0.1))
```
### Supplementary Material
---
The supplementary material can be found in Supplementary Materials.docx.
