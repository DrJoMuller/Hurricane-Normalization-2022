All raw data is available in CSV files, in addition to code, on github repository https://github.com/DrJoMuller/Hurricane-Normalization-2022
This study provides open access to all raw data used in the PL22 and CL22 normalizations for 2022. Please note that the normalizations will be updated to 2023 after the 2023 Current-Cost Net Stock of Fixed Assets and Consumer Durable Goods value is released by the BEA in 2024 (typically around September). As also noted in the paper, the below adjustment methodology for PL22 and CL22 following the methodologies documented in Pielke and Landsea (1998) and Collins and Lowe (2001), respectively, with a modification for how the population and housing units adjustments are made. 

a) Historic Storm Losses
	We used both Weinkle et al., (2018) and Grinsted et al. (2019) in order to determine the top 50 costliest storms. We then constructed a new dataset that sources the base economic damages for those top 50 storms between 1900-1979 from the original reports (see GitHub repository “Historic Losses”). These damage records are mostly from Monthly Weather Review discussions of each storm, while several storms have updated damage numbers due to incomplete reporting of the original damages in Monthly Weather Review. Within this dataset each storm has an individual citation to the source of the damage estimate. We then use NCEI for storms from 1980 onwards. NCEI disaggregated damage is sourced from the individual National Hurricane Center Tropical Cyclone Reports. In two cases the NCEI disaggregated damages are only available as ranges (Charley and Katrina's second landfalls) and in this case we use the median of those numbers. 

Our damage database is available in CSV file “1: Historic Losses Muller” in GitHub repository  https://github.com/DrJoMuller/Hurricane-Normalization-2022

Our new database also updates disaggregated losses for Hurricane Sandy after Aerts et al. 2013, Chesapeake Potomac Hurricane of 1933 using data from Klotzbach et al. (2021) who noted that Cobb (1991) had a much higher damage estimate than previous studies (e.g. Weinkle et al., 2018). Carla was updated based on a US Department of Commerce Report (US Department of Commerce, 1962). Agnes was updated on disaggregated state damage estimates from a USGS report (Bailey and Patterson, 1975). Freeport damage found Texas Hurricane History, National Weather Service, (Roth, 2010). Hazel is based on NOAA Technical Memorandum (Hebert and Taylor, 1983). 

Because there is not one agency reporting on hurricane damages through time, uncertainty arises in the consistency of the historical damage estimates between 1900-2022. See below “Damage Estimates Through Time”

Damage Estimates Through Time:
The economic damage estimates (landfall year) for each hurricane in this study are crucial for the normalized loss calculations and therefore, it is important to note the changing derivation of damage estimates between 1900-2022. From 1900-1979, damage estimates were largely obtained from the Monthly Weather Review (MWR). However, the MWR estimates represent a highly variable and subjective combination of losses from the American Red Cross, the U.S. Office of Emergency Preparedness, insurance companies and press reports (Blake, 1998). And the methodology used in calculating the estimates quoted in the MWR is not clear. Beginning in (at least) 1987, the National Hurricane Center (NHC) doubled insurance industry losses for individual storms as the basis for estimates of total damage (Blake et al., 1998; Weinkle et al., 2018). Examination of the relationship between insured damage to official NHC storm loss totals since 1987 indicates that the doubling practice was used as a guideline that was often modified rather than a formulaic application (Pielke et al. 2008; Weinkle et al., 2018). After 1994, except for a few cases involving significant flooding (e.g. Opal), most of the MWR damage estimates were determined by doubling the private insurance losses reported by the Property Claim Service (PCS) or the American Insurance Institute. These insurance loss figures do not include flood losses from the National Flood Insurance Program (NFIP), which began appearing in the MWR with Hurricane Ike in 2008 (Blake, 1998). Even though NFIP was launched in 1968. Beginning in the 1995 season the National Hurricane Centre (NHC) developed a more consistent methodology for NHC damage estimation, as the sum of double the insured loss estimate, plus an adjusted estimate of flood losses from NFIP. By 2016, NHC stopped providing estimates for direct economic losses (damage) and the National Centers for Environmental Information (NCEI) began reporting official US hurricane damage estimates generally utilizing the NHC “Billion Dollar Weather and Climate Disasters.” methodology (Blake, 1998). NCEI damage estimates account for “the insured and uninsured direct loss components include: physical damage to residential, commercial and government/municipal buildings, material assets within a building, time element losses (i.e., businesses interruption), vehicles, boats, offshore energy platforms, public infrastructure (i.e., roads, bridges, buildings) and agricultural assets (i.e., crops, livestock, timber). These loss assessments do not consider losses to natural capital/assets, healthcare related losses, or values associated with loss of life”. NCEI loss estimates reflect direct effects of weather and climate events (i.e., not including indirect effects) and constitute total losses (i.e., both insured and uninsured) (Smith et al., 2013). Generally, NCEI follows the same approach that NHC had developed in 1995 using the sum of double the insured loss estimate, plus an adjusted estimate of flood losses from NFIP. Because of the highly variable rates of flood insurance along the coast, it is improper to simply double the flood losses for an estimate of total flood damage.  Instead, the county NFIP losses are multiplied by the estimated county penetration rates for the highest flood risk area using the Federal Emergency Management Agency (FEMA) special flood hazard area (SFHA, e.g. the 100-year base flood plain) for a more accurate measure. This estimate should still be conservative for total flood damages because most homeowner’s policies are capped at $250,000 and areas outside of the SFHA can be affected in a significant flood (Blake 1998).  Note that NCEI relies on private insurance data that insurance agencies are contractually and legally obligated to not make public and for this reason the raw insured loss data, and subsequent disaggregation of NCEI calculated economic losses are not available publicly. Note that the NCEI calculations (1980-2022) are likely more comprehensive estimates than those provided in MWR for example (1900-1979). However, as mentioned above the methodology used in calculating the estimates quoted in the MWR (1900-1979) is not clear and may, or may not, include losses resulting from flood. 

This paper provides raw data for all publicly available damage datasets listed above (see appendix) however the calculations in the main text of the paper utilize mostly MWR estimates between 1900-1979 and use NCEI estimates from 1980-2022 (see appendix Muller et al damage column). Data source references are provided for each estimate. Due to the evolving damage methodology discussed above authors refrain from time series trend analyses of normalized losses. And readers, and users, of data should be aware of the possible inconsistencies in the historic damage estimate methodologies over time.

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

Raw county population data are available in CSV file “9: Population and Housing Data” 
The subsequent population adjustment factors are available in CSV file “11: Population and Housing Adjustments”

e) Housing Unit Adjustment
The housing unit adjustment was made to account for the change in housing units, within the counties impacted by a historic storm. Here we employed the same RMW method described above to identify coastal counties within the RMW field for each historic storm. We then obtained decadal county housing units data from the US Census Bureau and linearly interpolated between 1900-2000, with annual county data used from 2000 and 2022 (Census, 2022):
U.S. Census Bureau, 2020: Historical Housing Change Data (1910-2020), accessed September 30, 2023. These data are available in the above CSV files (9 and 11).

Then again using Spatial tools in ArcGIS Pro, we identified coastal counties that fell within 2*RMW field for each historic storm. This data is available in CSV file “8: GIS Generated Counties in 2_RMW”
Raw county population/housing units data are available in CSV file “10: Population and Housing Data_2_RMW” 
The subsequent population/housing units adjustment factors are available in CSV file “12: Population and Housing Adjustments_2_RMW”

f) Normalization Calculations
	The final normalization calculations using both the Pielke and Landsea (1998) and Collins and Lowe (2001) methods can be found in CSV files “13: Disaggregated PL22 and CL22 Normalizations_1RMW” and “14: Disaggregated PL22 and CL22 Normalizations_2RMW”
For rankings of the top 50 storms by CL22 see CSV file “15: Top 50 CL22”. For rankings of the top 50 storms by PL22 see CSV file “16: Top 50 PL22”.
To compare results between RM1 and RM2 normalization calculations see CSV file “17: Top 50 PL22”.

g) Alicia Example
Raw data from the Alicia normalization example are available in CSV file “18: Alicia Example”
