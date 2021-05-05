# Capstone Project Report

## Introduction

The New York Police department is interested in better understand how venues affect committed crimes, in order to be better prepared to prevent particular crimes in given venues.
The focus of the analysis is on the Manhattan borough, but future extended analysis may include all 5 boroughs of New York City.

## Data

To investigate the problem, we will use the following two data sources:

* [2014-2015 Crimes reported in all 5 boroughs of New York City](https://www.kaggle.com/adamschroeder/crimes-new-york-city?select=NYPD_Complaint_Data_Historic.csv)
* [The Foursquare API](https://foursquare.com/)

The __2014-2015 Crimes reported in all 5 boroughs of New York City__ dataset reports committed crimes in the 5 boroughs of New York along with several additional information, but for the purpose of this analysis the following information will be used:

* __OFNS_DESC__: textual description of the committed crime
* __Latitude__: position latitude of the committed crime
* __Longitude__: position longitude of the committed crime

The __The Foursquare API__ allows to retrieve venues information from latitude and longitude of a given place. In partucular, given the latitude and longitude coordinates of a place, the API can retrieve a list of nearby venues along with many information. For the purpose of the analysis the following information will be considered.

* __venue name__: the name of the venue
* __venue category__: the category of the venue such as Bar, Restaurant, Market, Hotel, etc

The analysis will leverage on the latitude and longitude of committed crimes provided by __2014-2015 Crimes reported in all 5 boroughs of New York City__ to retrieve the list of nearby venues categories using __The Foursquare API__.

## Methodology

discuss and describe any exploratory data analysis that you did, any inferential statistical testing that you performed, if any, and what machine learnings were used and why.

As the problem we are trying to solve is a classification problem, we will leverage on the __KMeans__ algorithm to cluster crimes categories using nearby venues category. An example of a data point for the __KMeans__ algorithm is given below:

| Crime         | ATM           | Accessories Store  | Auto Garage  | Beach    | other venues categories |
| ------------- | ------------- | ------------------ | ------------ | -------- | ----------------------- |
| FORGERY       | 0.000000      | 0.008798           | 0.002933     | 0.016949 |  |

where each number indicates the mean of the frequency of occurrence of each venue category for the given crime.

## Results

Using the __KMeans__ algorithm the crimes categories has been clustered into 5 groups. The following images eports excerpts of each cluster:

### Cluster 1
[](https://raw.githubusercontent.com/DocBrown85/AppliedDataScienceCapstone/main/images/cluster_1.JPG)

### Cluster 2
[](https://raw.githubusercontent.com/DocBrown85/AppliedDataScienceCapstone/main/images/cluster_2.JPG)

### Cluster 3
[](https://raw.githubusercontent.com/DocBrown85/AppliedDataScienceCapstone/main/images/cluster_3.JPG)

### Cluster 4
[](https://raw.githubusercontent.com/DocBrown85/AppliedDataScienceCapstone/main/images/cluster_4.JPG)

### Cluster 5
[](https://raw.githubusercontent.com/DocBrown85/AppliedDataScienceCapstone/main/images/cluster_5.JPG)

## Discussion

discuss any observations you noted and any recommendations you can make based on the results.

## Conclusion

conclude the report.
