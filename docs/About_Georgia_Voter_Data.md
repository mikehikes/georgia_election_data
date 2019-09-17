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
