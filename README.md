# Crime-Chronicles-Inflation-in-the-Golden-State
Project 1: Investigating the possible connections between inflation and fluctuations in crime activity within California.



## Project Overview
The overall purpose of this project was to investigate as to whether there was a correlation between fluctuations in inflation and fluctuations with crime within California over a 25 year time period (1998 - 2023). The data used in this investigation consisted of the crimes reported from the California Department of Justice, as well as the inflation rates of those years collected from Investopedia. We would begin first by investigating how crime overall has fluctuated througout the 25 year time period, and then break them down into distinct crime categories (Violent, Larceny, and Property). From these three categories, we would then investigate how each changed over time, and then compare these trends to the changes in inflation throughout the years. 

# Research Questions:
This investigation would conduct itself with the intent of answering these four questions:

How have crime rates in California changed from 1998 to 2023?

What are the long-term trends in different types of crime (e.g., violent crimes, property crimes) over this 25-year period?

Is there a correlation between annual inflation rates and overall crime rates in California over the past 25 years?

How does inflation impact different types of crime (e.g., theft, burglary, assault) over this period?

## Resources
The data collected on crime statistics from the years 1998 to 2023 was obtained from Open Justice - California Department of Justice and detailed the crimes broken down into categories and their respective counts each year. [Open Justice - California Department of Justice](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Resources/US_Inflation_Rates_1998_to_2023.csv)

The data collected on inflation rates in the United States from the years 1998 to 2023 was obtained from Investopedia which detailed the inflation rates, as well the events that were believed to contribute to these rates, for each year from 1998 to 2023. [Investopedia - Inflation Rates](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Resources/US_Inflation_Rates_1998_to_2023.csv)

## MainScript
The code used in developing our analysis is stored in the file [VisualizationData](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/VisualizationData.ipynb) as a jupyter notebook.

# Analysis
A condensed version of this analysis was organized into a [powerpoint presentation](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/Communal%20Resources/Crime_Chronicles_ppt_final.pptx), however the detailed analysis is written below:

The initial steps in this investigation focused on answering as to how crime rates changed over the years. This was done through the creation of a line graph that depicts the total count of all crimes commited in California in each year as seen below:

![Total Crimes Over 25 Years](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Total%20Crimes(25%20Years).png)

Note that the numbers were exceedingly high, essentially in the millions, that the graph was made into a logarithmic scale for ease of reading. This particular graph also shows that onwards from 1998, crime experienced a relative decrease over time, despite certain upticks. This trend would continue and maintain its decrease all the way to the end of the time period.

However, in order to get a better understanding as to how crimes had fluctuated over time, it would be prudent to break down the crime counts by categories, in order to see if there were variations in the trends amongst different types of crimes. The breakdown of these crime trends are shown in the picture below:

![Scaled Crime Counmt](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Scaled%20Crime%20Count.png)

This line graph has three lines color coded by type of crimes: Violent, Property, and Larceny. The data we had found from the California Department of Justice broke down the differing crimes from these three main categories, and as such we took the counts from these columns in order to more easily represent types of crimes based on easily recognizable categories. This grouping by category allows us to then compare these types of crimes towards inflation fluctuations and see the level of severity crimes change in response: i.e., do fluctuations in inflation cause more severe violent crimes (e.g., homicide), or less severe crimes like larceny(e.g., petty-theft). Take note of the fact that this particular graph was scaled through a MinMaxScaler in order to better depict the fluctuations between these categories. The reason for this was due to the fact that each major category had drastic differences in their total count, with the counts for property crimes eclipsing Larceny and Violent Crimes. However, despite their differing relative size, each experienced similar decreases, and increases over time, except for after 2018, which may be due to outside factors.

In order to answer the questions as to how inflation rates affect these types of crimes, graphs depicting each category alongside the fluctuation of inflation rates were made as seen below:

![Inflation vs. Violent Crimes](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs%20Violent%20Crimes.png)

This graph depicts violent crimes versus inflation rates and was found to have a correlation of approximately 0.2. This would mean that there was a slight positive correlation between changes in inflation and changes in violent crimes, with an increase in inflation leading to an increase in violent crimes.

![Inflation vs. Robbery](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Robbery.png)

This graph depicts larceny versus inflation rates and was found to have a correlation of approximately -0.2. This would mean that there was a slight ne correlation between changes in inflation and changes in larceny crimes, with an increase in inflation leading to a decrease in larceny crimes.

![Inflation vs. Property Crimes](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Property%20Crimes.png)

this graph depicts property crimes versus inflation rate and was found to have a correlation of approximately -0.2. This would mean that there was a slight negative correlation between changes in inflation and changes in property crimes, with an increase in inflation leading to a decrease in property crimes.

What is interesting to note in these graphs, is that whaile they all share similarly weak trends, however, it did not allow us to understand as to why property crimes and larceny crimes experienced a negative correlation to inflation. We suspected that there might be some form of outlier within the data that may be causing these correlations. A box plot was then made in order to discover these possible data outliers, which is depicted below:

![Box Plot of Inflation Rates](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Box%20Plot%20of%20Inflation%20Rate.png)

Through this box plot of inflation rates we noticed two outliers that corresponded to the inflation rates for the years 2021 and 2022, and so we believed that these data points were skewing the data in a meaningful way. Using this knowledge we then ommitted these data points in a reconficuration of the categorical crimes against inflation rates, as depicted below:

![Inflation vs. Violent Crimes(Omissions)](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Violent%20Crimes%20(Omissions).png)

This graph shows a stronger positive correlation between violent crimes increasing alongside inflation rates as seen in thea areas where those two data points were omitted, however when we checked its correlation, we found that it only incrased slightly to a 0.3 value. Which would mean that while there was an increase in the strength of positive correlation it was not enough to state that there was a definite strong correlation between inflation and violent crimes.

![Inflation vs. Robbery(Omissions)](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Robbery%20(Omissions).png)

This graph shows how the omission of the data points affected the inflation rate trend alongside larceny crimes. When the correlation coefficient was checked for this graph, it was shown that it had actually flipped and became approximately 0.2, which would mean that larceny crimes and inflation actually had slightly positive correlation, which is more in keeping with the data trends we see.

![Inflation vs. Property Crimes(Omissions)](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Property%20Crimes%20(Omissions).png)

This graph shows how the omission of the data points affected the inflation rate trend alongside property crimes. Similar to the larceny correlation coefficient, the inflation and property crimes was approximatley 0.2, which would mean that property crimes and inflation actually had a slightly positive correlation.

# Conclusion:
There is a slight positive correlation between increases in inflation and increases in crime. This correlation suggests that there are outside factors that more heavily influence the increase in crimes than inflation.


