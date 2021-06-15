# 2021 NYC election data

Hello! This repository hosts a table of all the NYC Election Districts (read: precincts) and the electoral regions they fall under (EDtable.csv). I compiled and joined it based on tables obtained through multiple data requests from the [NYC Board of Elections](https://vote.nyc/). 

## Source
I made email requests to the NYC BoE's Candidate Records Unit and received two excel documents and one text table containing the data I needed. See "Raw docs" folder for the originals. Note that all files are marked "TENTATIVE SUBJECT TO CHANGE". According the BoE, the source data is current for 2021.

## Table format
| Election District  | County | Borough | Assembly District | City Council District | Tagged as unused |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| string, official format | string, sentence case | string, sentence case | string, number | string, number | boolean, TRUE if tagged |

## "Unused" EDs

Of the 5901 EDs in NYC, there were 236 tagged as 'unused' EDs by the election department. I've used the "tagged as unused" column to indicate which these were. 

For example, 064/64 and 070/64 in Staten Island were marked as 'unused'. See them at the intersections of other boundaries in this excerpt of an [official election district map](https://vote.nyc/sites/default/files/pdf/maps/ad/ad64.pdf). ![image](https://user-images.githubusercontent.com/6442309/116641916-8e851280-a922-11eb-9363-850f9bef5390.png)

## Notes on overlapping boundaries

### City Council districts that straddle boroughs
| CC District  | Borough 1 | Borough 2 | notes |
| ------------- | ------------- | ------------- | ------------- |
| 8  | Bronx  | Manhattan  | A spatially even divide between East Harlem and South Bronx  |
| 22  | Bronx  | Queens  | Includes Rikers Island (Bronx), and is otherwise fully in Queens  |
| 34  | Brooklyn  | Queens  | none  |

### State Assembly Districts that straddle boroughs
Only AD 64, which is mostly Eastern Staten Island but also includes the northern part of Bay Ridge, Brooklyn.

* * *
### Let me know if you have suggestions or found it useful! [rogerlem.com](https://rogerlem.com)
