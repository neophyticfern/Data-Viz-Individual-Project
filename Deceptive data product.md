---
title: 'Design of Deceptive Data Product - Vox Gun Violence Charts'
author: 'Neville Fernandes'
output: html_document

---

This is the documentation for the creation of a deceptive data product, taking the same data as used in developing the various charts in Vox’s article on the gun violence problem in America (Lopez, 2018). Here, I have created three different visuals in an attempt to find out or display some findings in an interesting, non-trivial, and somewhat unexpected fashion. All three visuals are charts created using Tableau, labeled as Deceptive data product - 1, 2 and 3 and accessible here - https://public.tableau.com/profile/neville.fernandes#!/. The making of the three visuals is detailed below.


**Visual 1: More guns result in fewer deaths from guns**

The data for this chart was sourced from an article from the Guardian on gun homicides and gun ownership across the world (Chalabi, 2012). The link to the data is here -  https://docs.google.com/spreadsheets/d/1chqUZHuY6cXYrRYkuE0uwXisGaYvr7durZHJhpLGycs/edit#gid=0. Here we plotted the Homicides by firearm rate (per 100,000 people) with the Average firearms rate (per 100 people) and added a trendline to show how the homicide rate is correlated to the rate of firearm ownership. The Average firearms rate was added to the “Column” field and Homicides by firearm rate was added to the “Row” field (SUM was applied to both measures). The countries were selected based on a certain high-level of income, but intentionally so as to tilt the reference line to show a negative correlation between homicide rate and firearms rate. Additionally, the United States data point was annotated as well, to show the location with respect to the trend line and the rest of the data. 

**Visual 2: Responsible gun ownership in America**

The data for this chart was sourced from the same source as above (Chalabi, 2012). Three new fields were calculated from the original data - % of total guns in the world, % of total firearm homicides in the world and ratio of gun deaths to number of firearms. The details of the calculations are given below –

	% of total guns in the world = [Average total all civilian firearms] * 100 / 644,008,400
		where 644,008,400 is the total number of guns in the world
		
	% of total firearm homicides in the world = [Number of homicides by firearm] * 100 / 127,607
		where 127,607 is the total number of firearm homicides in the world

	Ratio of gun deaths to number of firearms = [Homicide by firearm rate] / [Average firearms]
		where the ratio is per 1000 people.

The visual is actually two charts, placed one over the other. The “Column” field in both charts is the Country dimension. The first chart shows a list of countries on the x-axis and % of total firearm homicides in the world and % of total guns in the world on the left and right y-axes respectively. Both of these measures were inputed into the “Row” fields and then the Dual Axis option was applied to the latter. For the bottom chart, we used the third measure as calculated above in the “Row” field. These charts were juxtaposed so that the countries were arranged in descending order of total firearm homicides in the world.

**Visual 3: Fewer guns doesn’t lead to fewer homicides in Australia**

The data was sourced from the website of the Australian Bureau of Statistics, which covers the various causes of death in Australia (3303.0 - Causes of Death, Australia, 2017). The file downloaded is an Excel file attached for Intentional self-harm (Suicide) (Australia). We used the data from sheet “Table 11.5”, which had the list for deaths by suicide for the year range of 2007-2016, from which the data for All Persons was manually transposed into a CSV file. Thus, we obtained the various categories of suicide as our measures (attributes) and the years as dimensions for our chart. From here, the measure of Firearms and Total were used in the “Row” field in Tableau and the years were used as the dimension in the “Column” field. The two measures were then combined in a Dual Axis. 
The caption covers a fact on rise in gun ownership, which was taken from the website GunPolicy.org (Alpers & Rosetti, 2018). 


### References

+ 3303.0 - Causes of Death, Australia. (2017, Spetember 27). Retrieved from Australian Bureau of Statistics: http://www.abs.gov.au/AUSSTATS/abs@.nsf/DetailsPage/3303.02016?OpenDocument
+ Alpers, P., & Rosetti, A. (2018, May 4). Australia Firearm Imports (Number) - Customs. Guns in Australia: Firearm Imports (Number) - Customs. Sydney School of Public Health, The University of Sydney, New South Wales, Australia: GunPolicy.org. Retrieved from GunPolicy.org: http://www.gunpolicy.org/firearms/compareyears/10/firearm_imports_number
+ Chalabi, M. (2012, July 22). Gun homicides and gun ownership listed by country. Retrieved from The Guardian: https://www.theguardian.com/news/datablog/2012/jul/22/gun-homicides-ownership-world-list
+ Lopez, G. (2018, May 18). America’s unique gun violence problem, explained in 17 maps and charts. Retrieved from Vox: https://www.vox.com/policy-and-politics/2017/10/2/16399418/us-gun-violence-statistics-maps-charts


