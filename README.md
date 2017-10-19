# data-512-a1
Niharika Sharma

## The goal of the project
The goal of this project is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through September 30 2017 following the best practices for open scientific research in designing and implementing our project, and make our project fully reproducible by others: from data collection to data analysis.

For this project, we combine data Wikipedia traffic from two different Wikimedia REST API endpoints into a single dataset, perform some simple data processing steps on the data, and then analyze that data.

Step 1: Data acquisition  
Step 2: Data processing  
Step 3: Analysis  
Step 4: Documentation  

For running and replicating the final visualization, install all the packages correctly as mentioned in the jupyter notebook and run the Jupyter Notebook. 


## Final Visualization 
![alt text](https://github.com/niharikasharma/data-512-a1/blob/master/PlotPageviewsEN_overlap.png)


## License of the source data
[License: MIT](https://opensource.org/licenses/MIT)


## [The Wikimedia Foundation terms of use (LINK)](https://wikimediafoundation.org/wiki/Terms_of_Use/en)


## Link to all relevant API documentation
1. [Legacy Pagecounts API] (https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts) - The legacy Pagecounts API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)) provides access to desktop and mobile traffic data from January 2008 through July 2016.  
2. [pageview API] (https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews) - The Pageviews API ([documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoint](https://wikimedia.org/api/rest_v1/#!/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through September 2017.

## Final data file

### Relevant files for final csv file
We collect data for all months from both pagecount and pageview APIs and then save the raw results into 5 separate JSON source data files (one file per API query).  
pagecounts_desktop_site_200801_201607.json  
pagecounts_mobile_site_200801_201607.json  
pageviews_desktop_201507_201709.json  
pageviews_mobile_app_201507_201709.json  
pageviews_mobile_web_201507_201709.json  

### Final file is the en-wikipedia_traffic_200801-201709.csv file in data directory and the description of the values of all fields in the final data file is as follows:

Column | Value | description |
| ------------- |:-------------:| -----:|
year | YYYY | year on English Wikipedia from January 1 2008 through September 30 2017 |
month | MM | month on English Wikipedia from January 1 2008 through September 30 2017 |
pagecount_all_views | num_views | Total number of (desktop + mobile) views from pagecount API  |
pagecount_desktop_views | num_views | Total number of desktop views from pagecount API |
pagecount_mobile_views | num_views | Total number of mobile views from pagecount API |
pageview_all_views | num_views | Total number of (desktop + mobile) views from pageview API |
pageview_desktop_views | num_views |  Total number of desktop views from pageview API |
pageview_mobile_views | num_views |  Total number of mobile (web + app) views from pageview API |


## Known issues or special considerations with the data 
Data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not.
