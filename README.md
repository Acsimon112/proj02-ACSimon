# Project 02 Proposal: <your project title>

**Team members:** <name(s)>

See the [Project 02 instructions](https://data385.github.io/project/proj02_wholegame.html) for what goes in each section. Bullet points are great. Put any images in an `img/` folder.

## 1. Problem statement

Preventable death is always a problem no matter where you go, that is no different in California. I want to see what causes are highest and where so I can figure out where best I can fund or start programs that will help counteract those preventable deaths. More importantly, I wanted to see if population had anything to do with it.


## 2. Research question

"Does the population of a county affect the leading cause of death present within that county?"


## 3. Data acquisition

I'll be collecting my death data from the california health and human services open data portal, in csv format. If need be, I can collect census data to verify populations and perform a join by county name or something similar.


### a. Confirm viability

_Scraping: summarize the "Before You Scrape" checklist. Downloading: citation, link to the documentation, and how the data were originally collected. Collecting it yourself: how you are collecting it and where you are storing it._

I'll be collecting my data through california government agency websites:
https://data.chhs.ca.gov/dataset/58619b69-b3cb-41a7-8bfc-fc3a524a9dd4/resource/2e546f88-bba8-4d77-846a-7fb77846cac6/download/2026-10_deaths_provisional_county_month_sup.csv

https://data.ca.gov/@california-health-and-human-services-agency/calhhs-data-de-identification-guidelines-reference-dataset/r/d3e02ccd-9081-453d-85dc-7f70df4907bd


### b. Variables of interest

_If you do not have the data yet, list the variables you plan to collect and the exact question text. Include 1) the variable name, 2) data type 3) description. Use bullet points._

from the death dataset:
- county: categorical variable. String. the county the death was recorded in.
- cause: categorical variable. String. cause of death in a 3 letter code
- cause_desc: Same as cause, except it states a full description of the cause of death. More readable.
- cause_density: Numerical. I'll have to make this one myself to pull the density of the causes of death for each county.

from census data:
- county: name of the county. Useful as a join operator.
- population: numeric. Will be used to gauge the population of a county.

## 4. Data example

_Scraping: a URL and an annotated screenshot. Downloading: a link to your rendered `data_management.pdf` with `glimpse()`. Collecting: a screenshot of one example row._

PDF in github repo.


## 5. EDA

_The techniques and functions you plan to use to import, wrangle, visualize, and explore the data, and why each is needed._

I'll import them from a data folder, which should be self explanitory. Using both datasets i'll probably perform a join to match leading causes of death to populations so that I can visualize it. I'll most likely be performing a visualization through a scatterplot based on a single cause of death perhaps. I'll need to take the density of these cases, and likely do some further wrangling. Perhaps another variable with death density and population to form a density per capita type observation. That might help ease problems with large population differences.


## 6. Modeling

_The models you plan to use, your response and predictor variables, and why the models fit your research question._
It's very possible I can take some leading causes of death in each county and then run a linear regression model to look for correlation between population and cause of death. This will fit my research question as I aim to spot any differences in population density and cause of death.

## 7. Communicate

_How you plan to present your results (website, poster, or short slide presentation)._

I'll be putting all of this on a quarto website most likely.


## 8. LLM disclaimer

_Whether and how you will use AI tools: the specific tool, its use, and your data protection methods. If you won't use any, say so._

