## SUMMARY

*Human Trafficking Destinations* presents data on countries cited as destinations of seven types of human trafficking labor between the years of 2001 and 2011. The data of this interactive visualization comes from the Human Trafficking Indicators, an open data project launched and maintained by Australian National University researcher Richard W. Frank. 

From the Human Trafficking Indicators (HTI) *Codebook*:

*The Human Trafficking Indicators database (HTI) codes information about human trafficking flows between 179 
countries and within them from 2000 to 2011.1 These data capture the various types of human trafficking found 
within a country as well as what its government is doing to prosecute traffickers, protect victims, and prevent 
further trafficking. It also codes whether states are primarily source, transit, or destination countries as well 
as if there is internal trafficking. The data are ordered by trafficking type and then according to the rough 
structure of the US State Department’s Trafficking in Persons (TIP) reports.*

## DESIGN 

### Objective 

For many, the term "human trafficking" connotes specific forms of forced labor, often sexual exploitation. Anti-human trafficking agencies, including the US State Department and United Nations Office on Drugs and Crime, maintain a broader defintion of forced labor, and this visualization seeks to illustrate how segmenting the verticals of the global black market reveals different traffic flows. 

The objective of this D3 visualization is to provide viewers with the opportunity to compare global patterns of human trafficking by mapping country destinations for the seven forced labor types tracked by the Trafficking in Persons (TIP) report published by the US State Department. 

### Design  

**Global trends over time**

The main impressions I am aiming for in this visualization is the tracking of regional and global spread for the selected forced labor type. This can be seen most notably when comparing *Prostituion* (global spread that increases over the 11 year period) with *Child Soldiers* (restricted regional growth over time). A bold yellow hue was selected to aid in this global tracking, yet national borders were clealry maintained, as the data is collected based on specific national anti-human trafficking tracking assessments. 

**Data types**

The Human Trafficking Indicators do not include population estimates or data on specific flow trajectories. It is for this reason why I chose not to higlight the data source's *Destination* data, and not its data on *Source* and *Transit*, as I found in my sketches that these comparisons encouraged a linearity in thinking of specific traffickig flow routes, which my research did not support. For instance, just because Mexico is listed as a *Source*, and the United States as a *Transit*, does not mean a trafficked person in the *Destination* of Canada came from that route. In fact, in-country forced labor (with no smuggling of persons) is a major issue for many countries, and storytelling on movement of persons can mask the impact of this problem. 

I chose, instead, to focus on the differences between specific labor types tracked in the HTI, which come directly from the data classifications outlined by the US State Department in the TIP reports. For each year, each country can receive only one of three values - a citation, no citation, or no data. These are each clearly displayed, 

**Geo Projection** 

I chose mercator, as relative geographic scale was not not necessary for my narrative, and I found the verticality of the flattening of the globe made the countries and continents more immediately legible than other projections such as *Natural Earth* or *ven der Grinten*. 

**Interaction**

To emphasize the individuality of the longitudinal devleopments of each labor type, I chose to offer the viewer a radio dial where they could select one labor type a time. After some user testing, I chose to disable the *Play* button during each animation to prevent the visualization from attempting to present two sequences at once.   


**FIRST iteration (index1.html)**

![Design #1] (https://cloud.githubusercontent.com/assets/19956669/22394041/e3383036-e4c9-11e6-9f80-ca1bf8946347.png)

* Begin with a blank map, title, legend, labor types and a *Play* button. 
* Select a labor type from a radio dial 
* Labor type selction reveals a brief description 
* Press *Play* to cycle through 11 years of global human trafficking destination data

**SECOND iteration (index2.html)**

![Design #2](https://cloud.githubusercontent.com/assets/19956669/22443396/996f6d62-e6f3-11e6-9569-8c617f51329d.png)

* Make years more visible
* Make 'Go' button more visible
* Perform additional data cleaning on nation geometry data (ensure "no data" really means "no data", not just different name) 
* Include introductory narrative the covers topic, data source, and different labor types 

## FEEDBACK

Between the first and second iterations I conducted the following three user interviews: 

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

