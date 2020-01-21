# Data

This project will utilize data from several sources:
1. Geospatial data will be gatherd from www.geonames.org
2. Census data from Statistics Canada https://www.statcan.gc.ca/
3. Current business/venue data from https://foursquare.com/

The geospatial and census data will be combined to form a larger dataset, the data will be joined by post code. Finally the FourSquare API will be used to identify restaurants within a 10KM radius. The responses from FourSquare will be cached due to rate limitations on the API.

Once all of the data has been gatherd, analysis can be preformed to identify the best types of cuisines for a new business to sell.

Preview of geospatial data:

|      | country code | postal code | place name                          | state name | state code | admin name2 | admin code2 | admin name3 | admin code3 | latitude | longitude | accuracy |
| ---- | ------------ | ----------- | ----------------------------------- | ---------- | ---------- | ----------- | ----------- | ----------- | ----------- | -------- | --------- | -------- |
| 0    | CA           | T0A         | Eastern  Alberta (St. Paul)         | Alberta    | AB         | NaN         | NaN         | NaN         | NaN         | 54.766   | -111.717  | 6        |
| 1    | CA           | T0B         | Wainwright  Region (Tofield)        | Alberta    | AB         | NaN         | NaN         | NaN         | NaN         | 53.0727  | -111.582  | 6        |
| 2    | CA           | T0C         | Central  Alberta (Stettler)         | Alberta    | AB         | NaN         | NaN         | NaN         | NaN         | 52.1431  | -111.694  | 5        |
| 3    | CA           | T0E         | Western  Alberta (Jasper)           | Alberta    | AB         | NaN         | NaN         | NaN         | NaN         | 53.6758  | -115.095  | 5        |
| 4    | CA           | T0G         | North  Central Alberta (Slave Lake) | Alberta    | AB         | NaN         | NaN         | NaN         | NaN         | 55.6993  | -114.453  | 6        |

Preview of census data:

|      | Geographic code | Geographic name | Province or  territory     | Incompletely  enumerated Indian reserves and Indian settlements, 2016 | Population, 2016 | Total private  dwellings, 2016 | Private dwellings  occupied by usual residents, 2016 |
| ---- | --------------- | --------------- | -------------------------- | ------------------------------------------------------------ | ---------------- | ------------------------------ | ---------------------------------------------------- |
| 0    | 1               | Canada          | NaN                        | T                                                            | 35151728         | 15412443                       | 14072079                                             |
| 1    | A0A             | A0A             | Newfoundland  and Labrador | NaN                                                          | 46587            | 26155                          | 19426                                                |
| 2    | A0B             | A0B             | Newfoundland  and Labrador | NaN                                                          | 19792            | 13658                          | 8792                                                 |
| 3    | A0C             | A0C             | Newfoundland  and Labrador | NaN                                                          | 12587            | 8010                           | 5606                                                 |
| 4    | A0E             | A0E             | Newfoundland  and Labrador | NaN                                                          | 22294            | 12293                          | 9603                                                 |