## SUMMARY

From HTI's Codebook : 

The Human Trafficking Indicators database (HTI) codes information about human trafficking flows between 179 
countries and within them from 2000 to 2011.1 These data capture the various types of human trafficking found 
within a country as well as what its government is doing to prosecute traffickers, protect victims, and prevent 
further trafficking. It also codes whether states are primarily source, transit, or destination countries as well 
as if there is internal trafficking. The data are ordered by trafficking type and then according to the rough 
structure of the US State Department’s Trafficking in Persons (TIP) reports.

## DESIGN 

The objective of this D3 visualization is to introduce people to the types of labor defined under the umbrella
term "human trafficking", and to highlight the global distribution of destinations of such exploitation. 

**First iteration (index.html)**

* Begin with a blank map, title, legend, labor types and go button. 
* Select a labor type, press 'Go' and cycle through 10 years of global human trafficking destination data
* Interactive radio button includes brief descriptions that display when type is selected 

**Second iteration (index2.html)**

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
* Boostrap: http://getbootstrap.com/css/
* ColorBrewer: http://colorbrewer2.org/#type=sequential&scheme=BuGn&n=3
