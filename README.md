# Georgia Election Data Repo

## About this Repository and Project History

Given the amount of news, interest, and focus on elections in the State of Georgia over the past two election cycles, I thought it would be helpful to acquire publicly-available data from the Georgia Secretary of State's office and determine what types of independent analysis I could conduct on my own. (In full disclosure, I am a resident of the State of Georgia). 

Code contained in the repo will be initially python3-based; however R or other languages may be used as needed. The code is engineered to operate on most mid- to high-powered laptops (in 2019, at least).

At the very least, this repository is designed as a template or toolkit for others to continue analysis on the source data. To this end, I will initially develop Jupyter Notebooks to conduct ETL of the data, and subsequent notebooks for analysis. Where sensible, Jupyter Notebooks that are script-like in nature will be converted to python scripts.  

## Current Projects

1. ETL Scripts to compile the voter data into a transaction-type databsae and a key-pair database, to indicate for each voter, their annual participation in elections. [Jupyter Notebook](https://https://github.com/mikehikes/georgia_election_data/tree/devwork1/etl)

2. An investigation on the observed percentage of voters who vote again in a future election, compared to a previous election. [Jupyter Notebook](https://github.com/mikehikes/georgia_election_data/blob/devwork1/analysis/Analysis%20of%20Repeat%20Voters.ipynb)

## Planned Projects

## Issues and errata

The issues tab of this repo will be the location for feature requests, bugs, and other items. 

## About the Georgia Voter Database

The State of Georgia's Secretary of State (SoS) Office provides a portal to download voter history data at https://elections.sos.ga.gov/Elections/voterhistory.do

There are two data sources of voter data available: one source contains a record of every time an eligible Georgia citizen votes, using a sequential voter registration number as the unique identifier for the voter. The second source is a table that matches the name and other demographic characteristics (required by law) with the sequential voter registration number. The prior data table is provided without cost, but the second data table is only accessible through payment of a $250 fee.  

The data accessible through the SoS web portal is provided from 1996 to the current time. 

This analysis will, for now, only review the first (non-cost) data source.

This table contains the following data, presented as a fixed-column-width string, with each line delimited by a `\n`:

The following columns are observed in the data:

1. Voter Registration Number
2. The Date of the Voter's Recorded Vote
3. A numeric code that indicates the type of election in which the voter participted (e.g., a primary, a general election, etc.)
4. If the voter voted in an election with a partisan primary vote, a letter indicator if the voter chose to vote in the Democratic (D), Republican (R), or Non-Partisan (NP) primary. 
5. An indicator if the ballot submitted was an absentee ballot.
6. For voting records from 2013 to present, an indicator if a ballot was provisional
7. For voting records from 2013 to present, an indicator if a ballot was supplemental

While the SoS web site indicates a single fixed-width schema for all data, there are in fact two schema: one for data prior to 2013, and one for data 2013 and onwards.
