# ETL (Extract, Transform, and Load) Notebooks of _State of Georgia Election Data_

## Overview

Elections data with limited demographic information is available from the State of Georgia's Secrectary of State is available [without cost](https://elections.sos.ga.gov/Elections/voterhistory.do). An enhanced version is available for a fee; this enhanced version has the name and address of the voter, along with the voter's self-reported ethnicity. 

The data is provided as a series of fixed with text files, of which two vintages are observed: data from 1996 until and including 2012, and data from 2013 onwards. Each row/record in the text files reflects a ballot submitted by a voter in the State of Georgia. 

## Vintage <=2012

This data contains the following fields:
1. Voter Registration Number
2. Election Type
3. Election Date
4. County Number
5. Binary indicator if the submitted ballot was an absentee ballot
6. Categorical indicator if the ballot was submitted for a primary election, and if so, the political party selected by the voter.
  * None _(If the election was not a primary or primary run-off)_
  * Democrat
  * Republican
  * Non-Partisan

## Vintage >=2013

This data contains the following fields:
1. Voter Registration Number
2. Election Type
3. Election Date
4. County Number
5. Binary indicator if the submitted ballot was an absentee ballot
6. Binary indicator if the submitted ballot was a supplemental ballot
7. Binary indicator if the submitted ballot was a provisional ballot
8. Categorical indicator if the ballot was submitted for a primary election, and if so, the political party selected by the voter.
  * None _(If the election was not a primary or primary run-off)_
  * Democrat
  * Republican
  * Non-Partisan
 
An individual ballot can be either an absentee ballot, supplemental ballot, or provisional ballot, but not more than one.

### Election Type

The _Election Type_ field is inconsistent from election to election and jurisdiction to juristiction. From what is observed in the data, a new election type is created for each agglomeration of different types of elections into a single election event.

For example, all general elections that contain only general election ballots have a single election type code. However, if a single election event in a jurisdiction contained more than one type of ballot (e.g., a special election and a general election held on the same day), then a new `election_code` will be generated.

I have collected all possible `election_type`s and manually assigned them to my own classification [on this repo](https://github.com/mikehikes/georgia_election_data/blob/devwork1/auxillary_files/election_type_mapping.csv).

