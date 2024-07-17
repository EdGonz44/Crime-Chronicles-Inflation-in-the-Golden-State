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

# Analysis
The initial steps in this investigation focused on answering as to how crime rates changed over the years. This was done through the creation of a line graph that depicts the total count of all crimes commited in California in each year as seen below:
![Total Crimes Over 25 Years](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Total%20Crimes(25%20Years).png)
Note that the numbers were exceedingly high, essentially in the millions, that the graph was made into a logarithmic scale for ease of reading. This particular graph also shows that onwards from 1998, crime experienced a relative decrease over time, despite certain upticks. This trend would continue and maintain its decrease all the way to the end of the time period.

However, in order to get a better understanding as to how crimes had fluctuated over time, it would be prudent to break down the crime counts by categories, in order to see if there were variations in the trends amongst different types of crimes. The breakdown of these crime trends are shown in the picture below:
![Scaled Crime Counmt](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Scaled%20Crime%20Count.png)
This line graph has three lines color coded by type of crimes: Violent, Property, and Larceny. The data we had found from the California Department of Justice broke down the differing crimes from these three main categories, and as such we took the counts from these columns in order to more easily represent types of crimes based on easily recognizable categories. This grouping by category allows us to then compare these types of crimes towards inflation fluctuations and see the level of severity crimes change in response: i.e., do fluctuations in inflation cause more severe violent crimes (e.g., homicide), or less severe crimes like larceny(e.g., petty-theft). Take note of the fact that this particular graph was scaled through a MinMaxScaler in order to better depict the fluctuations between these categories. The reason for this was due to the fact that each major category had drastic differences in their total count, with the counts for property crimes eclipsing Larceny and Violent Crimes. However, despite their differing relative size, each experienced similar decreases, and increases over time, except for after 2018, which may be due to outside factors.

In order to answer the questions as to how inflation rates affect these types of crimes, graphs depicting each category 
![Inflation vs. Violent Crimes](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs%20Violent%20Crimes.png)

![Inflation vs. Violent Crimes(Omissions)](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Violent%20Crimes%20(Omissions).png)

![Inflation vs. Robbery](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Robbery.png)

![Inflation vs. Robbery(Omissions)](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Robbery%20(Omissions).png)

![Inflation vs. Property Crimes](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Property%20Crimes.png)

![Inflation vs. Property Crimes](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Inflation%20vs.%20Property%20Crimes%20(Omissions).png)

![Box Plot of Inflation Rates](https://github.com/EdGonz44/Crime-Chronicles-Inflation-in-the-Golden-State/blob/main/group_project/Crime_Chron_images/Box%20Plot%20of%20Inflation%20Rate.png)





