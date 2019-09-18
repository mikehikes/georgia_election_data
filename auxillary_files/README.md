# Auxillary Files

## election_type_mapping.csv

The Election Type field is inconsistent from election to election and jurisdiction to juristiction. From what is observed in the data, a new election type is created for each agglomeration of different types of elections into a single election event.

For example, all general elections that contain only general election ballots have a single election type code. However, if a single election event in a jurisdiction contained more than one type of ballot (e.g., a special election and a general election held on the same day), then a new election_code will be generated.

This file contains these classifications, mapped to the `election_type` in the original data, with the original descriptions provided by the Secretary of State Office.
