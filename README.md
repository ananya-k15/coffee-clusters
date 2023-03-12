![header]()

This repository trains a supervised machine learning model to predict the best location to open a coffee shop in New Delhi for the IBM Applied Data Science Capstone Course by Coursera.

## Table of Contents

1. [Business Problem](#0)<br>
2. [Data Requirements and Sources](#1)<br>
3. [Methodology](#2)<br>
4. [Results](#3)<br>
5. [Scope for Further Development](#4)<br>
6. [References] (#5)<br>

## Business Problem <a id="0"></a>

Location of a coffee shop is one of the primary factors which determine its success. If any potential property developers are looking to build a coffee shop, where should they build it based solely on the location of nearby coffee shops ?

## Data Requirements and Sources <a id="1"></a>

Here is a list of the data requirements, and the sources used to obtain them :

| Requirement                                     | Source         |
| ----------------------------------------------- | -------------- |
| A list of all the neighborhoods in New Delhi    | Wikipedia page |
| The latitude and longitude of each neighborhood | Geocoder       |
| Coffee shops venues in a locality               | Foursquare API |

## Methodology <a id="2"></a>

1. Build a dataframe of neighborhoods in New Delhi, India by web scraping the data from Wikipedia page.

2. Get the geographical coordinates of the neighborhoods in New Delhi.
3. Obtain the venue data for the neighborhoods from Foursquare API
4. Explore and cluster the neighborhoods in Delhi.
5. Select the best cluster to open a new shopping mall

## Results <a id="3"></a>

We can see that neighborhoods that have the most number of coffee shops are at the heart of the city and the number of coffee shops per neighborhood decreases as we move away from the centre.

There are :

1. Most residential neighborhoods are in the first cluster since they don't have any coffee shops.
2. There are almost no coffee shops in cluster 1, while the second cluster has a moderate number of coffee shops.
3. A lot of neighborhoods have too many coffee shops, and belong to clusters 2 and 3.

Hence, there is great disparity in the distribution of coffee shops across neighborhoods. This shows that any potential investors would be better suited investing in clusters 0, 1 or 3.

## Scope for Further Development <a id="4"></a>

In this project, only one factor was considered: the frequency of occurrence of coffee shops in neighboring localities. In any future research, considering other features like neighborhood population and resident income will provide a comprehensive result. <br> Since project made use of the free SandBox Tier of the Foursquare API, it was limited to a specific number of API calls and results that could be returned. With a paid account these limitations can be bypassed to obtain much more holistic results.

## References <a id="5"></a>

Category: Neighbourhoods in Delhi Wikipedia retrieved from
https://en.wikipedia.org/wiki/Category:Neighbourhoods_in_Delhi <br>
Foursquare Developers Documentation Foursquare retrieved from
https://developer.foursquare.com/docs/
