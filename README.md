# High-Drinking-Sense

Code supporting my Undergraduate Work about finding  High Risk Drinking Locations, or vulnerable regions for alcohol consumption across cities using social media activity.

You can get more information by reading our pappers published at [CoUrb 2023](https://doi.org/10.5753/courb.2023.774) and [SBBD 2023](https://doi.org/10.5753/sbbd_estendido.2023.233144).

If you're interested in our dataset, you can find it on [Zenodo](https://doi.org/10.5281/zenodo.10037884).

Below I provide more technical details.

How it works
====================

All the code is written in Python 3 and dependencies can be install from [requirements.txt](requirements.txt). 

First we collect data from two social media, Foursquare and Twitter. Then we explore the data in order to create our database.

Finally we perform analysis in order to obtain classifications among the city.

Data collection
========================
### twitter_api.py
[twitter_api.py](collection/twitter_api.py) uses the Twitter API filtered stream service in order to retrieve tweets tagged with our requirements.

### filter.py
[filter.py](collection/filter.py) presents the filtering process used to gather information and obtain the database described bellow.

<ul>
  <li>Venue's ID on Foursquare</li>  
  <li>User's ID on Swarm</li>  
  <li>Venue's name</li>  
  <li>Venue's category</li>  
  <li>Venue's country</li>  
  <li>Venue's city</li>
  <li>Timestamp from post on Twitter </li>
  <li>Venue's latitude</li> 
  <li>Venue's longitude</li>
</ul>

### update.py
[update.py](collection/update.py) adapts our database to new necessities.

Data Analysis
========================
The jupyter notebooks used to perform all data analysis with our collected data and obtain all regions classification are available at [analysis](analisys). 

Alcohol Consumption
========================
The jupyter notebook used to perform all analysis envolving alcohol consumption is available at [alcohol](alcohol).

All the data used for the alcohol consumption analysis were extracted from [World Health Organization (WHO)](https://www.who.int/data/gho/data/themes/topics/sdg-target-3_5-substance-abuse), coresponding to the Sustainable Development Goal 3.5.2. 
