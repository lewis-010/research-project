# Analysis of Great Britain's Electrical Demand
This project aimed to determine if the operation and flexibility of pumped hydro energy storage (PHES) in Great Britain had been significantly impacted by the evolving energy sector. Energy storage is a crucial infrastructure of Great Brtain's electrical network, of which PHES makes up more 90% of installed capacity. Understanding how the usage of this technology will change in the coming years is critical to ensure it can efficiently aid the country in its net-zero ambitions.
<br/><br>

## Timeseries Analysis
The methodology for this project consisted of a literature review and an analysis of a timeseries dataset that represented Great Britain's real-time electrical demand from 2008 to 2021. This GitHub repo will cover the analysis of the [dataset](https://zenodo.org/record/7140904).

Discussion of the literature review and results is available in the *Research project.pdf*.

Required packages:
- pandas
- matplotlib
- pyarrow
<br/><br>

## Yearly Trends
- The first analysis *yearly generation.ipynb* focused on the yearly trends of electical generation from fossil fuels, major renewables and PHES.
- A column for YEAR was extracted from the utc_date column, this was then used to aggregate all data by the year. 
- It was then passed through the matplotlib.pyplot package to generate suitable figures.
- This gave an overall perspective on the recent long-term trends of the major electrical outputs in Great Britain.

<p align="center"> 
<img src="PNGs/Coal & Gas yearly generation.png" style="width: 330px"> <img src="PNGs/PHES yearly generation.png" style="width: 330px"> </p>

<p align="center">   
<img src="PNGs/Solar & Wind yearly generation.png" style="width: 330px">
</p>
<br/><br>

## Daily Output Trends
- The second analysis was focused on changes in the daily output trends of Great Britain's PHES facilities.
- This was done to identify changes in output patterns on a year to year basis by comparing the same month across various years. 
- Columns for both YEAR and DAY were extracted from ELEXM_utc date column. 
- These were the basis for using a multi-index format for the dataframe, allwoing for the comparison of the same months over various years in one figure.

<p align="center">
<img src="PNGs/PHES generation for January.png" style="width: 330px"> <img src="PNGs/PHES generation for April.png" style="width: 330px"> </p>

<p align="center">
<img src="PNGs/PHES generation for December.png" style="width: 330px">
</p>
<br/><br>

## Flexibility Analysis
- The final analysis aimed to identify trends in flexibility of the major power types.
- No formal method was found in literature or research so a novel process used to calculate flexiblity metrics for various electrical genration types.
- Taking the difference between set time intervals across a generation output line and totalling these values will give a value for how much that power type has varied over a certain time period.
- Doing this for all power systems enabled the calculation for how much flexibility each power type provides to the grid.
- (note - *espeni.csv* dataset replaced with *espeniWithNegPSValues.ztsd.parquet*. This included negative values for PHES when it removes/stores energy from the grid.)

<p align="center">
<img src="PNGs/Flexibility of major power types.png" style="width: 330px">
</p>
