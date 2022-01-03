# Semi-Structured Data - Analysing Customer Issues
![image](https://user-images.githubusercontent.com/75427181/147941729-6a454265-c2c9-4cfa-8e22-a6aab75acf4a.png)

## Introduction

This analysis was performed in order to understand the customer issues in the finance sector. Another objective is to understand the sources from which the issues where submitted. In addition, it will be determined from which state the issues came most frequently. The data are taken from Kaggle and contain information about customer issues in the US updated every week. 

## Exploring the data

The first step in the analysis is to check if the data contains any missed values in the important columns. There are 18 columns and important columns are the issues, the date and the state. All of those column does not have any missed values and require no further cleaning. However, it was detected that the there is no column for the year. This information has to be extracted from the date column. Further, many of the data are not needed and will be dropped in the beginning. A small part of the data can be seen below. 

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147941953-3b6873dc-fd3f-4340-9314-a284184d73dd.png" width="60%" height="auto" >
</p>
Figure 1: Overview Data

## Finding all Unique Issues

As the issue data are semi structured the first step is to find the unique problems that occurred during the years. For that the columns will be transformed into lower case and the strings will be spitted into each term. The finance related terms that were searched for can be found below. The analysis will be performed on each issue in every row.

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147942757-d723f442-58a7-4d78-bc7a-56ad98de9cdf.png" width="100%" height="auto" >
</p>

Figure 2: Unique Issues

## Hot Key Encoding of the Issues

For all of the defined finance word will be a column created contained with zeros. In case there is one issue in the row, it will be denoted as one (in the column with the same label). The columns look like the following.

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147942831-69a408b9-4d35-49c0-8472-a0825b69b10f.png" width="100%" height="auto" >
</p>
Figure 3: Hot Key Encoding

Next, the sum of the columns will be calculated. In order to gain a first overview, all the found issues will be displayed in a donut chart. 

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147943157-dbb7c057-98da-4ba5-8d60-c706e4565aeb.png" width="100%" height="auto" >
</p>
Figure 4: Overview Issues

From the bar chart it can be derived that the most common issue was related to loan and the credit card. The further analysis would require additional data to understand what happened in that cases. As those data are not available this step can only be performed theoretically.

To understand from which sources those data came from the different sources where determined. During this step it was detected that the mail data is split in email and postural. As those data are only available for the mailing data it will not be further analysed. 


<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147943282-67b866ee-ec36-4ad8-b7ee-40aef76baf36.png" width="100%" height="auto" >
</p>
Figure 5: Overview Submitted Via

To understand the development over time the data will be divided into each year. The problem is that there is no column containing only the year of the occurrence. This column was created by taking only the last four characters of the date column. The reason why this step was not performed earlier is that this calculation is time consuming and in this stage the data frame is smaller. Another interesting insight was found. The stored data increased largely over the years. This can be seen below. 

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147943500-97232611-8598-457a-8dc2-600edf9af1ad.png" width="60%" height="auto" >
</p>
Figure 6: Data Amount over the Years

The issues over the years can be seen in the following figure. It can be derived that the issues increased over the years. The most common issue during all the years was related to loan and credit cards. Furthermore, it was determined that the issues increase from 2011 up top 2015. This increase dropped by over 60 % in 2016. This could be explained because the Banks hired their own data scientist and are not interested anymore in submitting the data publicly. 

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147944228-5df952a3-cc05-4011-9e2c-c7fba4928e93.png" width="100%" height="auto" >
</p>
Figure 7: Development of the Issues
 
Net is the analysis of the submitted sources over the year. This can be seen in the figure below. From the figure it can be derived that the most used source to submit the issues is via the web. Therefore, if there are limited sources for building a customer issues service the web applications should have the highest priorities. 

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147943845-27dcc51b-ef08-42d9-b0b0-aef456e79286.png" width="100%" height="auto" >
</p>
Figure 8: Development of the Submitted Sources

At last the occurrence over the states in the US will be investigated. In the figure below can be seen that the most issues where submitted from California, Florida and Texas. 

<p align="center">
<img src="https://user-images.githubusercontent.com/75427181/147944024-2e90e51c-1246-48f6-8b85-61b62ca97a3c.png" width="100%" height="auto" >
</p>
Figure 9: Occurrence in the States

# Conclusion

Within the analysis it was determined that the most common customer issues were related to the loan and the credit cards. Furthermore, the most issues were submitted via the web. In case the company thinks about expanding their customer services it would be best to scale the web application. Lastly it was determined that most of the issues came from California and Texas. The reason could be that this states have the highest population in the US.  
