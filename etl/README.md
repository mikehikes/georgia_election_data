# ETL (Extract, Transform, and Load) Notebooks of _State of Georgia Election Data_

## Overview

Elections data with limited demographic information is available from the State of Georgia's Secrectary of State is available [without cost](https://elections.sos.ga.gov/Elections/voterhistory.do). An enhanced version is available for a fee; this enhanced version has the name and address of the voter, along with the voter's self-reported ethnicity. 

The data is provided as a series of fixed with text files, of which two vintages are observed: data from 1996 until and including 2012, and data from 2013 onwards. Each row/record in the text files reflects a ballot submitted by a voter in the State of Georgia. 

## Vintage <=2012

This data contains the following fields:
1. Voter Registration Number
2. Election Type
3. Election Date
4. Binary indicator if the submitted ballot was an absentee ballot
5. Categorical indicator if the ballot was submitted for a primary election, and if so, the political party selected by the voter.
  * None _(If the election was not a primary or primary run-off)_
  * Democrat
  * Republican
  * Non-Partisan

## Vintage >=2013

This data contains the following fields:
1. Voter Registration Number
2. Election Type
3. Election Date
4. Binary indicator if the submitted ballot was an absentee ballot
5. Binary indicator if the submitted ballot was a supplemental ballot
6. Binary indicator if the submitted ballot was a provisional ballot
7. Categorical indicator if the ballot was submitted for a primary election, and if so, the political party selected by the voter.
  * None _(If the election was not a primary or primary run-off)_
  * Democrat
  * Republican
  * Non-Partisan
 
An individual ballot can be either an absentee ballot, supplemental ballot, or provisional ballot, but not more than one.


