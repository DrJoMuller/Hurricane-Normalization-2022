This study provides open access to all raw data used in the PL22 and CL22 normalizations for 2022. Please note that the normalizations will be updated to 2023 after the 2023 Current-Cost Net Stock of Fixed Assets and Consumer Durable Goods value is released by the BEA in 2024 (typically around September). As also noted in the paper, the below adjustment methodology for PL22 and CL22 following the methodologies documented in Pielke and Landsea (1998) and Collins and Lowe (2001), respectively. 

a) Historic Storm Losses
The historic storm losses are taken from the Grinsted et al. (2018) supplementary documents: Grinsted, A., P. Ditlevsen and J. Hesselbjerg Christensen, 2019: Normalized US hurricane damage estimates using area of total destruction, 1900−2018, Proceedings of the National Academy of Sciences. https://doi.org/10.1073/pnas.1912277116 
These data were initially obtained by Grinsted at al from the ICAT database, which is no longer available. This data provided disaggregated losses for historic storm events, allowing for multiple loss calculations if a storm generated more than one loss (e.g., due to multiple landfalls). We have made some updates to this database that are highlighted in CSV file “1: Historic Storm Losses” 
The file indicates what was updated (2022 Updates), and from which source. We have made damage estimate additions for the more recent storm events not available at the time of the Grinsted et al. (2019) publication using the NCEI Billion Dollar Disasters database (NCEI, 2023). While we note that there may be challenges in working with this database, we are unaware of any other open-access databases from which we can make these additions. For transparency, the storms that are added using the NCEI database are Hurricanes Florence, Laura, Michael, Ida, and Ian. There is also an update to Sandy’s damage estimate because the Grinsted et al. damage estimate was not disaggregated by state in the ICAT database (Aerts et al. 2013). We also made updates where damage reports were limited to a single state erroneously. These storms are the Great New England (1938) and Great Atlantic (1944) Hurricanes using the update from Sumner (1944), Hurricane Carol (1954) using the update from Davis (1954) and Hurricane Floyd (1999) using the update from Blake and Landsea (2011).
Finally, we also updated damage from storms in which loss numbers in ICAT appeared to be inaccurate. The storms updated for this reason are Carla (1961) and the Chesapeake-Potomac (1933). The Chesapeake Potomac Hurricane of 1933 was updated using data from Klotzbach et al. (2021) who noted that Cobb (1991) had a much higher damage estimate for the hurricane than was used as the base damage estimate in Weinkle et al. (2018). Carla was updated based on a US Department of Commerce Report (US Department of Commerce, 1962). 

b) Inflation Adjustment
The inflation adjustment was calculated using the gross domestic product (GDP) deflator.  The GDP deflator is the price index used to measure changes in the overall level of prices for the goods and services that comprise GDP. This index is calculated as 100 times the ratio of nominal to real GDP (Williamson 2023). The GDP deflator data between 1900-2022 was obtained from Williamson (2023). 
Samuel H. Williamson, 'What Was the U.S. GDP Then?' Measuring Worth, 2023.
The inflation adjustment is simply the 2022 GPD deflator divided by the GPD deflator in the landfall year of the storm. This data is available in CSV file “2: Inflation”

c) Wealth Adjustment
The Current-Cost Net Stock of Fixed Assets and Consumer Durable Goods (CCNSFACDG) values were obtained from the U.S. Bureau of Economic Analysis:
U.S. Bureau of Economic Analysis, Current-Cost Net Stock of Fixed Assets and Consumer Durable Goods [K1WTOTL1ES000], retrieved from FRED, Federal Reserve Bank of St. Louis; https://fred.stlouisfed.org/series/K1WTOTL1ES000 , January 11, 2024. This dataset extends back to 1925.
Numbers before 1925 were calculated as 3% less that the preceding year following the approach of Pielke et al. (2008). The CCNSFACDG was divided by the CCNSFACDG in the landfall year of the storm. This data is available in CSV file “3: CCNSFACDG”
The CCNSFACDG must be adjusted for inflation and, depending on the method used, for US wide population (PL22) or US wide housing units (CL22). The inflation adjustment is the same as described above. In order to obtain yearly US population data, US Census Bureau decadal data between 1900-2000 were linearly interpolated, while annual data were available between 2000 and 2022 (Census, 2022):
U.S. Census Bureau, 2022: Historical Population Change Data (1910-2020), accessed September 30, 2023.
This data is available in CSV file “4: US Population”
Housing unit data are also provided by decade in U.S. Census reports. These numbers were manually entered from historic reports, which were not yet digitized and published by the agency, in spreadsheet format. Linear interpolation was used between housing unit decadal counts (U.S. Census 2020). 
U.S. Census Bureau, 2020: Historical Housing Change Data (1910-2020), accessed September 30, 2023.
This data is available in CSV file “5: US Housing Units”
The final wealth adjustment data are available in CSV file “6: Wealth Adjustment”

d) Population adjustment (PL22)
A population adjustment was made to account for the change in population, within the counties most likely to have been impacted by a storm. Here we employed a new method for determining coastal counties that were impacted by a storm. As outlined in the paper, we took the landfalling radius of maximum winds (RMWs) for each historic hurricane from HURDAT2 and inputted these RMWs into ESRI’s ArcGIS Pro Software: 
Landsea, C.W., J.L Franklin, J.L. Beven, (April 2013). The revised Atlantic hurricane database (HURDAT2) (Report). United States National Oceanic and Atmospheric Administration's National Weather Service. https://www.aoml.noaa.gov/hrd/hurdat/UShurrs_detailed.html Retrieved Jan 2024
These RWW data come from reanalysis work completed by:
Colón-Burgos, D. and C. W. Landsea (2023) Expanding the Atlantic Hurricane Database: Adding in Radius of Maximum Winds, American Meteorological Society Annual Meeting, 8-12 January 2023, Denver, Colorado
We followed the landfall definition as established by the National Hurricane Center: “the intersection of the surface center of a tropical cyclone with a coastline” (latitude and longitudes entered into in ArcGIS Pro obtained from HURDAT2):
Landsea, C.W., J.L Franklin, J.L. Beven, (April 2013). The revised Atlantic hurricane database (HURDAT2) (Report). United States National Oceanic and Atmospheric Administration's National Weather Servicehttps://www.aoml.noaa.gov/hrd/hurdat/hurdat2.html 
Using Spatial tools in ArcGIS Pro, we identified coastal counties that fell within the RMW field for each historic storm. This data is available in CSV file “7: GIS Generated Counties in RMW”
We then obtained decadal county population data from the US Census Bureau and linearly interpolated between 1900-2000, while annual county data were available between 2000 and 2022 (Census, 2022):	
U.S. Census Bureau, 2021: Historical Population Change Data (1910-2020), accessed September 30, 2023.
Raw county population data are available in CSV file “8: Population and Housing Data” 
The subsequent population adjustment factors are available in CSV file “9: Population and Housing Adjustments”

e) Housing Unit Adjustment
The housing unit adjustment was made to account for the change in housing units, within the counties impacted by a historic storm. Here we employed the same RMW method described above to identify coastal counties within the RMW field for each historic storm. We then obtained decadal county housing units data from the US Census Bureau and linearly interpolated between 1900-2000, with annual county data used from 2000 and 2022 (Census, 2022):
U.S. Census Bureau, 2020: Historical Housing Change Data (1910-2020), accessed September 30, 2023. These data are available in the above CSV files (8 and 9).

f) Normalization Calculations
The final normalization calculations using both the Pielke and Landsea (1998) and Collins and Lowe (2001) methods can be found in CSV file “10: Disaggregated PL22 and CL22 Normalizations”
For rankings of the top 50 storms by CL22 see CSV file “11: Top 50 CL22”. For rankings of the top 50 storms by PL22 see CSV file “12: Top 50 PL22”.

g) Alicia Example
Raw data from the Alicia normalization example are available in CSV file “13: Alicia Example”
