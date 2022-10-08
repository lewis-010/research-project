># Analysis of Great Britain's Electrical Demand
This project aimed to determine if the operation and flexibility of pumped hydro energy storage (PHES) in Great Britain had been significantly impacted by the evolving energy sector. Energy storage is a crucial infrastructure of Great Brtain's electrical network, of which PHES makes up more 90% of installed capacity. Understanding how the usage of this technology will change in the coming years is critical to ensure it can efficiently aid the country in its net-zero ambitions.
<br/><br/>

>## Timeseries Analysis
The methodology for this project consisted of a literature review and an analysis of a timeseries dataset that represented Great Britain's real-time electrical demand from 2008 to 2021. This GitHub repo will cover the analysis of the [dataset](https://zenodo.org/record/7140904). (note: *espeni.csv* dataset available on Zenodo adjusted to *espeni v2.csv*; day, month & year columns added)  

Required packages:
- pandas
- matplotlib
<br/><br/>

>## Yearly Trends
- The first analysis *yearly generation.ipynb* focused on the yearly trends of electical generation from fossil fuels, major renewables and PHES. 
- The half-hourly timeseries data was first aggregated by year and then passed through the matplotlib.pyplot package to generate suitable figures.

<img src="Coal & Gas yearly generation.png" style="width: 300px;"/>
<br/><br/>

>## Monthly Generation Comparisons


