# Federal-Reserve-Economic-Data-ETL-Pipeline-part_1-
The ETL-pipeline extracts economic indicators using the FRED API, and after that it stores them in a star schema in a data warehouse to research the relationship between energy and inflation.

Energy prices are rising tremendously, and we use more energy now than ever. With inflation also increasing, I wanted to research the correlation between them. In part two of this project, I will analyze the correlation and extend the pipeline for deeper research on data centers.

<img width="2070" height="705" alt="image" src="https://github.com/user-attachments/assets/3a199292-5064-447b-b5f2-c8468f7051f5" />

The architecture of this pipeline extracts the needed data, transforms them, and loads them into a star schema.
In the data model we have one fact table and three dimensions .I kept the date dimension unconnected because I join on the date column directly; a date_id link is a planned improvement.

<img width="861" height="657" alt="image" src="https://github.com/user-attachments/assets/786df5b2-eb90-46bb-9e4a-e5240b5d4f8e" />

How to run the script. I don’t know yet.

What I have learned throughout this project is that the first lines of code are easy, but after 40 lines you regret what you wrote in the beginning. I also learned that decisions and design choices are important before writing code you have to think about how the final main() is going to look, so also thinking about the extensibility of the pipeline and whether it works in one go or if you want to split it into three pieces.
I chose the star‑schema data model because I wanted it to be simple, and this research didn’t need complexity but efficiency.


Sources — National series
**Indicator ==	URL**
General_CPI 	== fred.stlouisfed.org/series/CPIAUCSL  		
CPI_energy ==	fred.stlouisfed.org/series/CPIENGSL 
Electricity_price_per_kWh == fred.stlouisfed.org/series/APU000072610 
Natural_gas_(Henry_Hub_spot) == fred.stlouisfed.org/series/DHHNGSP 
WTI_crude_oil	==	fred.stlouisfed.org/series/DC01LWTICO 
Recession_indicator ==	fred.stlouisfed.org/series/USREC 






