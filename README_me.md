# Nepal_Climate_change Assignment solution

## Assignment Solution Structure
The solution of assignment includes following files
1. Readme_me file: Readme file
2. GIS_Data_Science_assignment2.ipynb: Assignment solution file
3. data: folder containing shapefile and climate data.

## Objective
The objective of this assignment is to assess the understanding and practical skills in GIS Data Science, specifically focusing on climate data analysis for Nepal. The assignment deals with data reading, visualization, and exploratory data analysis (EDA) tasks using Python.

## Required libraries
install the required libraries with pip install command.
pip install numpy, pandas, matplotlib, seaborn, geopandas, geoplot

## Data source
shape data from: https://github.com/Desmondonam/Nepal_Climate_change
   This data includes political boundaries of Nepal upto local bodies (Gupalika and Nagarpalika). The district boundary is used for analysis of the Temperature and Precipitation data.
temperature and precipitation data from: https://opendatanepal.com/dataset/district-wise-daily-climate-data-for-nepal
   This data includes climate data of Nepal from Jan-1981 to Dec-2012 for each district collected at the end of the month.
   This dataset includes 18 environmental data fields. But for this assignment only two data fields are used
   "PRECTOT" is the  Precipitation (mm day-1)
   "TS" is the Earth Skin Temperature (C)   

## Processing steps
1. Download shape file for the political boundaries of Nepal and temperature and precipitation data from above sources and save it in the /data folder inside the assignment folder. The shape file is under Shape_Data folder and environment data is in climate_data_nepal_district_wise_monthly.csv file
2. read shape file from geopandas and get district boundaries from the given data.
3. read environmental data from geopandas and filter the required fields (temperature and precipitation data) from the given data. 
4. make Choropleth of temperature and precipitation data
5. make line plot of average yearly temperature and precipitation data of overall Nepal
6. make bar plot of average temperature and precipitation data from 1981 to 2019 for each districts of Nepal

## Findings from EDA
1. The shape file includes boundary of 777 local bodies of Nepal
2. The shape file includes boundary of 77 districts of Nepal
3. From plot of the district boundaries it is found that the shape file represents the latest political boundary of Nepal.
4. The envirnment data includes 18 environmental data fields for each district collected at the end of the month from Jan-1981 to Dec-2012
5. The envirnment data is available for only 62 districts of Nepal
6. There is no missing value in envirnment data
7. the value of envirnment data fields are stored as string. These values needs to be converted into numeric for analysis.
8. The DISTRICT of shape file is in uppercase characters while DISTRICT of envirnment data is in lowercase. For merging these geolocation data and envirnment data uppercase DISTRICT is used.
9. Before January 2018 the precipitation data is reported as an accumulation, after it is in average rate.

## Insights from visualizations and analysis of climate data for Nepal
1. From Choropleth plot we can see that temperature of southern part of Nepal is higher than northern part.
2. Temperature of East-Southern part of Nepal is higher than other part of Nepal
3. Comparing temperature of Nepal at Jan-2019 and Jan-1981 from Choropleth plot, over the period of data collection the average temperature of Nepal is in increasing trend. This is shown by the legend of the Choropleth.
The range of temperature at Jan-1981 is from -15C to 10 C whereas at Jan-2019 the range is from -10C to 15C
4. From Choropleth plot we can see that Precipitation in Nepal is in increasing trend from East to West with highest value around the southern part of the mid-Western part of Nepal. The trend is similar in Choropleth plot of both Jan-1981 and Jan-2017.
5. As opposed to the temperature value the Precipitation of nepal has decreased from Jan-1981 to Jan-2017 as indicated by the legend of the Choropleth.
6. From line plot of yearly average temperature of Nepal, it is seen that temperature was in increasing trend from 1981 to around 1999 then temperature starts declining. Also in some year variation in temperature is high where as it is low in some years.
7.  From line plot of yearly average Precipitation of Nepal, it is seen that Precipitation was in decreasing trend from 1981 to around 1999 then it starts increasing upto 2017. After January 2018.
 the precipitation is reported in average rate as opposed to accumulation so sharp drop in precipitation value is observed.
8. From bar plot of districtwise average temperature of Nepal, it is seen that Humla and Solukhumbu has -ve agerage temperature and all other districts has +ve agerage temperature. Except these districts Mugu has the lowest agerage temperature and Routahat has the highest agerage temperature.
9. From bar plot of districtwise average Precipitation of Nepal, it is found that the district with lowest and highest Precipitations are Humla and Ilam respectively.