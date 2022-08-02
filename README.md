# Label_Airplay_Map

## Background
**Mascot Label Group** is an independent Dutch record label, specializing in guitarists and associated genres (rock, metal, blues, etc). Since 2014, the label's North American office has pushed over 20 singles to rock radio from several artists including **P.O.D.**, **Black Stone Cherry**, **Crobot**, and **10 Years**. The purpose of this project is to identify trends in radio support for singles, artists, and the label overall based on data from individual radio stations.

## Requirements and Technology
This project required data to be downloaded from Mediabase, and used the following technologies:

* Excel/Google Sheets
* Python (Pandas Library)
* Tableau

## Overview
Song reports for every Mascot Records Active Rock radio single were downloaded as xlsx files from Mediabase. Some songs had two files, one for every year of its chart run, and looked like the following:

![Original_Mediabase_Report](https://github.com/heartgears/Label_Airplay_Map/blob/main/Mediabase_Report.png)

These song files were converted to CSV files and cleaned (month plays were deleted leaving only year totals, and each row was given a song, artist, and a year column) and concatenated into one csv file for Tableau to read and visualize. 

![Cleaned_Mediabase_Report](https://github.com/heartgears/Label_Airplay_Map/blob/main/Cleaned_Mediabase_Report.png)

The final step before visualizing was adding zip codes to every radio station for Tableau to be able to map each station appropriately using a VLOOKUP.

## Results
The final airplay dashboard appeared as follows:

![Mascot_Radio_Dashboard](https://github.com/heartgears/Label_Airplay_Map/blob/main/Dashboard_Screenshot_1.png)

The tooltip over the radio map includes format of the radio station, its market rank, location, callcode, and its total spins (filtered by the selections on the right). The dashboard is responsive and can filter data based on date range, artist, song, and station, allowing an in depth analysis of stations, artists and songs.

### Song Analysis
![Song_Demo](https://github.com/heartgears/Label_Airplay_Map/blob/main/Novacaine.png)

### Artist Analysis
![Artist_Demo](https://github.com/heartgears/Label_Airplay_Map/blob/main/10_Years.png)

### Station Analysis
![Station_Demo](https://github.com/heartgears/Label_Airplay_Map/blob/main/Station_Demo.png)

## Limitations and Improvements
While the dashboard is robust, it doesn't allow for easy comparisons betweens tracks, artists, etc. It requires one to make notes of the data displayed before visualizing another. 

The data input could also be improved by increasing the data from just years to month and year, allowing for a more granular analysis of a song's chart run.
