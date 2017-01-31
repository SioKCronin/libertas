## SUMMARY

*Human Trafficking Destinations* presents data on countries cited as human trafficking destinations for seven types of human trafficking labor types for years between 2001 and 2011. The data comes from the Human Trafficking Indicators (HTI), an open data project launched and maintained by Australian National University researcher Richard W. Frank. 

From the Human Trafficking Indicators (HTI) *Codebook*:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp The Human Trafficking Indicators database (HTI) codes information about human trafficking flows between 179 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp countries and within them from 2000 to 2011.1 These data capture the various types of human trafficking found 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp within a country as well as what its government is doing to prosecute traffickers, protect victims, and prevent 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp further trafficking. It also codes whether states are primarily source, transit, or destination countries as well 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp as if there is internal trafficking. The data are ordered by trafficking type and then according to the rough 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp structure of the US State Department’s Trafficking in Persons (TIP) reports.*

## CONTENTS

* **README.md**: This document
* **HTI.csv**: Original data downloaded from Human Trafficking Indicators  
* **data.json**: json output of Cleaning.ipynb
* **index1.html**: First design iteration
* **index2.html**: Second design iteration
* **world_countries.json**: Country geometries used from a World Cup example from my Udacity coursework 
* **labor_types.json**: Labor types with brief descriptions 
* **Cleaning.ipynb**: Reconcile world_countries.json with HTI.csv

For country geometry, I have used a datafile used in a World Cup example from my coursework at Udacity. This required some hand-corrections for countries whose names differed from my HTI data. These changes are documented in Cleaning.ipynb

## DESIGN 

### Objective 

For many, the term "human trafficking" connotes specific forms of forced labor. Anti-human trafficking agencies, including the US State Department and United Nations Office on Drugs and Crime, maintain a rather broader defintion of forced labor. This visualization seeks to illustrate how segmenting the verticals of the global black market reveals different traffic flows, which can ultimately help support national and global efforts to liberate people from exploitation. This visualiation provide viewers with the opportunity to compare global patterns of human trafficking for the seven forced labor categories tracked by the Trafficking in Persons (TIP) report published by the US State Department. 

### Design  

**Global trends over time**

The main impression I am aiming for in this visualization is the global spread of human trafficking by each of the highlighted forced labor categories. Variations in regional and global spread can be observed when comparing labor types. This can be seen most notably when comparing *Prostituion* (global spread that increases over the 11 year period) with *Child Soldiers* (restricted regional growth over time). To help the viewer keep track of the global spread, I selected a bold yellow hue for the citation data. I also kept national borders clearly maintained, as I wanted to provide viewers with the opportunity to monitor specific countries in their exploration. 

**Data types**

The Human Trafficking Indicators do not include population estimates or data on specific flow trajectories. I chose to higlight *Destination* data by itself, and not *Source* and *Transit*, as I believe the data source does not provide enough dimensionality to tell clear stories connection *Source*, *Transit*, and *Destination*. For instance, in 2011, Canada, Mexico, and the United States are each cited as *Source*, *Transit* country, and *Destination* for *Prostitution*. The data does not provide information as to how trafficking flows manifest between these countries, so presenting *Source*, *Transit*, and *Destination* is ambiguous. It would be difficult to ensure viewers are drawing conclusions that are consistent with the dynamics of the trafficking observed. Furthermore, in-country forced labor (with no smuggling of persons) is a major issue for many countries, and storytelling on movement of persons can mask the impact of this very serious problem. 

I chose, instead, to focus on the differences between global patterns of specific labor types, with data presenting the nations where people are actually held in the bondage (*Destination*). For each year, each country can receive only one of three values - a citation, no citation, or no data. I selected a bold yellow color for the citation, and contrasted this with a light blue color for the countries not given a citation. I indicated the countries with no data for the indexed year with a white fill.  

**Geo Projection** 

For my map projection, I chose mercator. Relative geographic scale is not necessary in the narrative I've chosen, and I find the verticality of land mass in mercator projections aid in readily identifying countries and continents, as compared to more 3D-evoking projections such as *Natural Earth* or *ven der Grinten*. 

**Interaction**

To emphasize the individuality of the longitudinal devleopments of each labor type, I provide the viewer with a radio dial where they could select one labor type a time. After some testing, I chose to disable the *Play* button during each animation to prevent the visualization from attempting to present two sequences at once, as this does not render successfully in the visualization as I have designed it.   


**FIRST iteration (index1.html)**

![Design #1] (https://cloud.githubusercontent.com/assets/19956669/22394041/e3383036-e4c9-11e6-9f80-ca1bf8946347.png)
Key features:

* Begin with a blank map, title, legend, labor types and a *Play* button. 
* Select a labor type from a radio dial 
* Labor type selction reveals a brief description 
* Press *Play* to cycle through 11 years of global human trafficking destination data

**SECOND iteration (index2.html)**

![Design #2](https://cloud.githubusercontent.com/assets/19956669/22443396/996f6d62-e6f3-11e6-9569-8c617f51329d.png)

Key feature changes: 

* Make years more visible
* Make 'Go' button more visible
* Perform additional data cleaning on nation geometry data (ensure "no data" really means "no data", not just different name) 
* Include introductory narrative the covers topic, data source, and different labor types 

## FEEDBACK

Between the first and second iterations I conducted three user interviews, which yielded the following recommendations: 

**Patrick [VR Engineer, 35] - Jan 26, 2017**
* Liked yellow as the hotbed activity color
* Wanted to see the year bigger to track its change 
* Wondered if there could be more data (hover over for country data)
* Wanted something playing at the start (consider martini glass/narrative intro)
* Consider a heat mapping - percentage of years assessed in which the country was cited (resulting in a 10 year cumulative picture at the end) 

**Philip [Health Care Educator, 39] - Jan 26, 2017**
* "It's hard to see the years advancing."
* "I don't know all of these countires. Like what's that one? [points to Sudan]"
* "Oh, I didn't see that 'Go' button down there." 

**Carl [Developer, 38] - Jan 27, 2017**
* "I want to feel like I get a sense of intensity of activity over time."
* "What countries am I looking at here? Like where's Syria in all of this?"
* I like that I can choose the labor type. 

## RESOURCES 

* Human Trafficking Indicators: https://humantraffickingindicators.org/
* US State Department: https://www.state.gov/j/tip/rls/tiprpt/
* International Labour Organization: http://www.ilo.org/global/about-the-ilo/newsroom/news/WCMS_181961/lang--en/index.htm
* Boostrap: http://getbootstrap.com/css/
* ColorBrewer: http://colorbrewer2.org/#type=sequential&scheme=BuGn&n=3
* Comparing Map Projections: https://bl.ocks.org/syntagmatic/ba569633d51ebec6ec6e

