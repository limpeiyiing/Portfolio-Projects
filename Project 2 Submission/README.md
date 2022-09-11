
# Project 2: Modelling Ames Housing Data and Kaggle Challenge  

## Project Statement:

**The client**: An owner of an up and coming property agency interested to break into the property market in Ames, Iowa.  

**Task**: Prepare a preliminary study of the market to evaluate feasibility of the business expansion. Will derive insights from the dataset through graphical visualizations and Linear Regression modelling. The best model that can best predict sales prices will be determined by RMSE and R2 Scores. 

**Objectives of the study**:
1) Provide an overview of the locale and general trends in the Ames residential property market. 
2) Identify the top predictors of residential property Sale Price in Ames

The results of this study will help the client evaluate if the company's current expertise and specialization is a good match to perform well in the Ames residential property market. 

## Background:
Ames is a city in Story County, Iowa, United States, located approximately 30 miles (48 km) north of Des Moines in central Iowa. It is best known as the home of Iowa State University (ISU), with leading agriculture, design, engineering, and veterinary medicine colleges. 

According to the 2020 census, Ames had a population of 66,427, making it the state's ninth largest city. Iowa State University was home to 33,391 students as of fall 2019, which make up approximately one half of the city's population. [[Wikipedia]](https://en.wikipedia.org/wiki/Ames,_Iowa)

Ames is a tight-knit city anchored by Iowa State University, and is ranked as one of the nation’s top college towns and earned the #33 spot on Livability’s list of the Top 100 Best Places to Live in 2022. It’s a top city for entrepreneurs thanks to its proximity to the research university, affordable living costs and its high-wage job growth. [[Livability]](https://livability.com/best-places/10-awesome-cities-with-little-to-no-traffic-yes-really/ames-ia/)

## The dataset:
The dataset used is a collection of 2032 observations (after cleaning) of properties sold in Ames, Iowa between 2006-2010. 

51% of the properties sold in this dataset are 1-story Houses, 29% are 2-story houses and 10% are 1.5 story houses (with finished 2nd level). 

In terms of general zoning classification, 78% of the houses sold were in low-density residential areas while 15% were in medium-density residential areas. 

While the distribution of property Sale Prices in Ames tends to skew to the left (towards lower-priced homes), the distribution of price per sqft of above ground living area is normally distributed with a mean of $121.13 psf.

There are nearly 80 variables in this dataset that describe property features, but for a preliminary analysis we will only zoom into the top few predictors of Sale Price. 

For more details on the dataset, please refer to the documentation [[here]](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt)




## Findings:

Buyers of residential properties in Ames, Iowa highly value:
1) Above Ground Living Area 
2) Overall Quality of the Material and Finish of the house
3) Recently built properties. Older properties sell for less. 

Properties in different neighborhoods are also valued differently, based on size, property age, demographics and proximity to desired amenities. 

Houses closer to downtown (and therefore the Iowa State University) tend to be priced lower compared to those in more northwards neighborhoods. 

This study has also found that remodelling doesn't significantly increase Sale Price, and the age of property at sale remains a stronger predictor of price. This would be an important consideration for house-flippers who intend to buy low, remodel, and then sell high. 

## Future Studies:

1) More detailed analysis on other (potential) price predictors in the dataset (such as number of rooms, garage condition, fireplaces, etc) in order to better refine the Linear Regression model. The better the predictive power of the model, the smoother the price negotiation process, the better the agency can serve its clients. 

2) To collect and analyze more data related to other price predictors, such as neighborhood demographics and nearby amenities
