---
layout: post
title: Exploring and Analyzing National Rural Health Mission Data
author: Harish Garg
categories: [Data Analysis]
tags: [Python, Data Analysis]
published: true
---

![Cover Image](/assets/images/map-state-maha.jpeg)

# Introduction

This purpose of this Data analysis is to identify the root causes of the extreme Health trends in Nagpur.

## About the data set

Data set received is an archive file which have a collection of Excel files. This data set is from the National Rural Health Mission, Maharashtra. The data belongs to Nagpur District, divided by the rural blocks in the district.

The archive, when extracted gives us 13 folders named as Blocks. Looking at the names of these folders, it seems to suggest each folder is for each of the rural blocks or tehsils in Nagpur district. Although, the wikipedia page lists 14 tehsils for Nagpur, divided between urban and rural, the data set doesn't have a folder for Nagpur Urban as it's expected from rural blocks.

Doing a recursive search tells us there are 376 files in total. Each excel file has data for one Health Center.
I decided do some initial exploratory analysis in the excel itself.

The data has five main parts.

- REPRODUCTIVE AND CHILD HEALTH
- Other Programmes
- Health Facility Services
- Monthly Inventory Status
- Mortality Details

Thehe # 4, i.e. Monthly Inventory Status has no actual data in there, so we are going to ignore that.
The rest of the 4 heads can be basically categorized into 2 broad level categories -

1. Health Programmers undertaken & services provided
2. Outcomes measured in terms of mortality under various heads.

## Cleanup and Data Reshaping

Here, I decided to use Python and pandas module for data import, cleanup & data reshaping. The following scripts were written for this purpose.

1. data_parser.py - main script to be called.
2. nhfm_parser.py - module with cleaning functions called by above script

To run this, run command "python data_parser.py" from command line.

Before running this script, I would recommend keeping the data folder at the same location at the script and check the data folder name in the script is same as your data folder.

This script will produce a xls file which will contain the data from all the xls sheets in a single sheet. I have decided to include data for the whole year and not month data because for lot of indicators, the month data is zero. I feel for this analysis, year level total data is sufficient.

I have also included the result file which was produced during my cleanup called "cleaned_full_data.xlsx", which can be used for your own analysis.
Analysis & Trends

For the analysis part, I decided to use Tableau Public. I connected the above xls file to the Tableau Desktop Public. Here are some of the observations which were made as part of the analysis.

## Maternal Mortality

Looking at the Maternal mortality plot by block, it's clear that except for 3 blocks, maternal mortality numbers are zero. However, we see that HIngna Block has a very high maternal deaths. In the next section, we will take a look at this block in more detail.

If we look at the population data from India's 2011 Census for Nagpur District blocks, we see that the Nagpur Rural and Hingna are the blocks with biggest population. But surprisingly, we don't have records for Maternal deaths for Nagpur Block.

Next, we look at the deliveries performed in Private vs Public institutions..

So, we have Hingna block with high maternal deaths, Deliveries at Public Institutions very low and deliveries at Private Institutions very high. On the other hand, we have Nagpur block having low maternal deaths, high proportion of deliveries performed at Public institutions and low proportion of deliveries at Private institutions.
Further, we plot the maternal mortality in Hingna block by the Health Center. We see that Digdoh SC and Raipur PHC have higher number of maternal deaths then the other Health Centers.

### Infant Mortality up to 5 weeks

Looking at the above plot, we see that infant mortality up to 5 weeks is quite high in Hingna and Nagpur blocks, as compared to other blocks. To dig deeper into this, we will plot these blocks separately at a Health Center level.
Like the maternal deaths analysis above, here also Digdoh SC and Raipur PHC has a high number of infant mortality deaths up to 5 weeks. We need to take a look at whether this is because these Health Centers much higher population than other Health Centers or there is some other cause which needs to be looked into.

In the Nagpur block, majority of the Infant deaths up to 5 weeks were reported from a single Health Center i.e. WH Nagpur. This needs further analysis on why there is a such a high incidence of infant deaths up to 5 weeks from this single Health Center.

### Adolescent/ Adult deaths

Here we look at the adolescent/ Adult deaths reported at block level during the period.
Katol block has the highest number of deaths reported in this category. So we will plot Katol at Health Center level.
This plot shows that PHCs at Kachrisawanga, Kondhali & Yenava have reported the highest number of adolescent/ adult deaths. And Respiratory deaths seems to be biggest cause of death here. This needs to be further analyzed on why is such a high prevalence of fatal respiratory diseases in these blocks.

### Child Immunization

Number of Health Centers by block

## Conclusion

To summarize, we can make below inferences from this data set.

- Hingna Block has a high maternity related deaths as compared to other blocks. It could be due to higher population of this block compared. Although, correlation is not causation, but it's hard to ignore the indicator that proportion of deliveries performed at private institutions in this block are much higher compared to other blocks with lesser maternity deaths. It would be useful to get some data on the maternal deaths which happened in private institutions vs. in public institutions.
- Hingna, again, along with Nagpur Block has a high number of Infant mortality compared to other blocks.
- Katol block has the highest number of deaths reported for adolescent/adults. And the real outliers in this block are the PHCs at Kachrisawanga, Kondhali & Yenava that have reported the highest number of adolescent/ adult deaths. Also, respiratory deaths seems to be biggest cause of death here. This needs to be further analyzed on why is such a high prevalence of fatal respiratory diseases in these blocks.
- Even though Hingna and Nagpur blocks has the highest population, they do not have the highest number of Health Centers. Infact Nagour Rural has less then half of the number of Health Centers then the the block with the highest number of Health centers.
- Hingna and Nagpur blocks were the blocks who performed best in the time period for immunization children under 2 years.
Last, but not least, this is very important to add this is not an exhaustive analysis. There are lot of trends and insights which can be gained from this dataset, especially comparing it with the latest National Family Health Survey Data and comparing how Nagpur as a whole is doing as compared to other districts in Maharashtra.