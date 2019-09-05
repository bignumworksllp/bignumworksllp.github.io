---
layout: post
title: Analyzing India's Missing Kids Data 
author: Harish Garg
categories: [Data Analysis]
tags: [Data Analysis]
published: true
---

![Cover Image](/assets/images/missing.png)

# Introduction

Go to the profile of Harish Garg
Harish Garg
Data Analyst & Software Developer, Passionate about Data Science, Machine Learning, AI
Feb 17, 2017
India’s missing: An analysis

So recently I was looking for Public government datasets in India for download and to analyze, that came across this Indian Central government website where people can report missing kids and their sightings in India.

They have a real time dashboard which shows number of missing kids(or persons?) by state.

Few odd things stood out to me.

For example…

Look at the Top states/UTs by total absolute number of missing…
Top 10 States / UTs by Total absolute missing

![Missing Kids by State](/assets/images/missing-kids02.png)

There are some expected names in there, like Uttar Pradesh, Bihar, Maharashtra, being that they big states.

However, you see some unexpected names too, like Chandigarh, for example. Why a small UT like Chandigarh has so many reported missing?

Let’s plot the missing per lakh population…

![Plot - Missing Kids by State](/assets/images/missing-kids03.png)

Chandigarh and Daman Diu really catches your eye in this. They are extreme outliers in this chart.

Now, the question arises, why is rate of missing being reported as high from these 2 UTs as compared to other states / UTs?

*Is it really because Chandigarh and Daman & Diu have a epidemic of missing? or Is it because people are confident in reporting the missing in these areas and th issing go really un-reported in other parts of the country? This is worrying to ecause then that means the actual missing are many times over.*

This is a Citizen reported dataset. So, I would consider it far away being complete. However, with whatever data is available, there are some questions which arise here that needs to be explored further.