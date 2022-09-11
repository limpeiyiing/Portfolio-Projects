# Project 4: Predicting West Nile Virus Infection of Mosquitos in Chicago  

*by Edward, Keziah, Pei Yiing*

## Background
In the United States, the West Nile Virus is one the most common mosquito-borne disease [(source)](https://www.cdc.gov/mosquitoes/about/mosquitoes-in-the-us.html#:~:text=West%20Nile%20virus%20is%20one,Virgin%20Islands%2C%20and%20American%20Samoa.). Since its initial discovery in the country in 1999, it has rapidly spread throughout the country when an infected mosquito bites a human. In September 2001, the disease was initially discovered in two dead crows in Illinois. In contrast to the 149 cases and 19 deaths reported to the CDC cumulatively from 10 states during the three years from 1999 to 2001, the first significant WNV outbreak in the United States was observed in 2002, when more than 4,150 human cases and 284 deaths attributable to WNV infection were reported from 40 states.

Although the majority of WNV carriers have no symptoms, one in five infected individuals have fever and other symptoms. Additionally, one in 150 infected individuals develops a serious, occasionally deadly illness[(source)](https://www.cdc.gov/westnile/index.html?CDC_AA_refVal=https%3A%2F%2Fwww.cdc.gov%2Fwestnile%2Ffaq%2FgenQuestions.html). 

A [study](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3322011/)  conducted based on the 2005 WNV outbreak in Sacramento County, California - where 163 human cases were reported - estimated the economic impact of the outbreak to be **\$2.28 million** for medical treatment and patients productivity loss for both West Nile fever and West Nile neuroinvasive disease. In addition, the emergency vector control applied for that outbreak cost **$701,790** including spray procedures and overtime hours.   

The cost-benefit analysis also indicated that only **15 cases** of West Nile neuroinvasive disease would need to be prevented to make the emergency spray cost-effective.

There are no vaccinations or treatments available currently for WNV in humans. Spraying pesticides would be one of the most effective ways to stop the virus, and by locating the potential hotspots and best time window to apply vector control, we can strike a good balance between cost and preventability.

In 2004, a thorough surveillance and control program had been built by the City of Chicago and the Chicago Department of Public Health (CDPH), and it is still in use today. Mosquitoes caught in traps placed throughout the city from late spring through the fall are examined weekly for the virus. The outcomes of these tests determine when and where the city will spray insecticides into the air to reduce adult mosquito populations[(source)](https://www.kaggle.com/c/predict-west-nile-virus/).

## Project Statement:

**The audience**: Decision-makers and executives of Chicago Department of Public Health

**The Task**: 
1) Train and evaluate a model that can predict the presence of the West Nile virus among mosquitoes in Chicago. The final model will be selected based on sensitivity, because the health and economic costs of wrongly predicting the status of a WNV-positive location, is higher than the vector control costs of predicting a WNV-negative location as WNV-positive. 

2) Based on EDA of the dataset and insights from the model, will perform cost-benefit analysis to recommend vector control strategies to best reduce WNV infection, at the least cost possible.  

## The Dataset

The dataset used for this study was provided by the Chicago Department of Public Health. 

| Dataset | Content                                                                                                                                             | Source                                            | Year                   |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|------------------------|
| Train   | -   Date -   Trap Location -   No. of mosquitos caught -   Species of mosquitos -   Presense of West Nile Virus                                     | Chicago   Department of Public Health             | 2007, 2009, 2011, 2013 |
| Weather | -   Date -   Temperature -   Humidity-related measurements -   Type of Weather -   Wind speed/direction -   Atmospheric pressure -   Sunrise/Sunset | National   Oceanic and Atmospheric Administration | 2007 - 2014            |
| Spray   | -   Date -   Time -   Location/Latitude                                                                                                             | Chicago Department of Public Health               | 2011 - 2013            |

## Findings

1. We built 5 classifier models to predict incidence of WMV based on data collected across 4 years, and selected the **XGBoost Classifier** based on its' sensitivity of 85.7%. The model identified the following **features** with high importance:  
   a) The week in which sample of mosquitos was collected  
   b) Weather conditions: Rain, Mist  
   c) Trap cluster   
   d) Species of Mosquito  
   
   
2. We also performed cost-benefit analysis to identify potential strategies to focus vector control efforts, mainly by:  
   a) Identifying seasonal trends for WNV - we propose that **active surveillance and vector control efforts begin in mid-July, subject to weather conditions.** 
      - Warmer temperatures would mean a shorter *Culex* mosquito life cycle, which would mean we need extra cycles of vector control. 
      - Higher than usual precipitation at the end of June would also indicate an early start of the season of breeding and infection, which translates to the need to start vector control in early July.  
        
   
   b) Identifying **clusters of trap locations as hotspots to focus vector control efforts**, whether by increasing frequency of spraying or applying other methods that are more effective.
      - 59 trap locations were identified as hotspots (reported WNV infections in at least 2 years out of the 4 surveyed) or spots with recent activity (reported WNV infection in 2013). 
      - By managing these hotspots more effectively, we will reduce spread of the virus to other locations, minimizing the need for extensive vector control (and therefore, costs) in the long run

## Future Works

1. Refine the selected model to increase sensitivity by:  
     a) **Re-enginnering current features**. For example, instead of taking rolling 3-day averages of weather features, we could attempt to see if better results can be obtained with rolling 7-day averages of weather features.     
     b) Adding more features based on existing dataset. Eg: **Wind Speed, Wind Direction and other specific weather conditions (thunderstorms, squall, mist or fog)**  
     c) Collecting and studying additional data for additional features, such as **geographical features, effect of vector control efforts or distribution/density of specific bird species that act as carrier hosts.**   

2. Build and evaluate a **Recurrent Neural Network** model to test if it provides better sensitivity than the current XG Boost model. 