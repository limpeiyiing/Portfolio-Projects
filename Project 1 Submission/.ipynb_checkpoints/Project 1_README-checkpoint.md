# Project 1:  Improving SAT Participation Rates across the United States

## Project Statement:

We are interested to identify opportunities to increase SAT participation rates across the United States by:

- Exploring trends in SAT participation rates across 50 US states across 3 years (2017-19)
- Identifying relationships between SAT participation rates and other factors such as SAT scores and ACT participation rates

At the end of this study, we aim to identify opportunities for investment by zooming in on specific states. We will also propose focus areas based on the relationships to the factors highlighted above. 

## Scope
The following data dictionary summarises the dataset used in this study:

| Column   Name     | Data Type | Dataset | Year    | Description                                                                                                                                                             | Range                                                         |
|-------------------|-----------|---------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| act_comp_2017     | float64   | ACT     | 2017    | ACT composite scores                                                                                                                                                    | 1.0 - 36.0                                                    |
| act_comp_2018     | float64   | ACT     | 2018    | ACT composite scores                                                                                                                                                    | 1.0 - 36.0                                                    |
| act_comp_2019     | float64   | ACT     | 2019    | ACT composite scores                                                                                                                                                    | 1.0 - 36.0                                                    |
| sat_ebrw_2017     | int64     | SAT     | 2017    | Average score for Evidence-based   Reading and Writing section                                                                                                          | 200 - 800                                                     |
| sat_ebrw_2018     | int64     | SAT     | 2018    | Average score for Evidence-based   Reading and Writing section                                                                                                          | 200 - 800                                                     |
| sat_ebrw_2019     | int64     | SAT     | 2019    | Average score for Evidence-based   Reading and Writing section                                                                                                          | 200 - 800                                                     |
| sat_math_2017     | int64     | SAT     | 2017    | Average score for Math section.   Range                                                                                                                                 | 200 - 800                                                     |
| sat_math_2018     | int64     | SAT     | 2018    | Average score for Math section.   Range                                                                                                                                 | 200 - 800                                                     |
| sat_math_2019     | int64     | SAT     | 2019    | Average score for Math section.   Range                                                                                                                                 | 200 - 800                                                     |
| sat_total_2017    | int64     | SAT     | 2017    | Average Total score, sum of EBRW   and Math section                                                                                                                     | 400 - 1600                                                    |
| sat_total_2018    | int64     | SAT     | 2018    | Average Total score, sum of EBRW   and Math section                                                                                                                     | 400 - 1600                                                    |
| sat_total_2019    | int64     | SAT     | 2019    | Average Total score, sum of EBRW   and Math section                                                                                                                     | 400 - 1600                                                    |
| name              | object    | ALL     | -       | Names of 50 US states. Excludes:   District of Columbia                                                                                                                 | 50 states                                                     |
| act_part_2017     | float64   | ACT     | 2017    | State ACT participation rate for   a given year                                                                                                                         | 0.00  - 1.00                                                  |
| act_part_2019     | float64   | ACT     | 2019    | State participation rate                                                                                                                                                | 0.00  - 1.00                                                  |
| act_part_2018     | float64   | ACT     | 2018    | State participation rate for a   given year                                                                                                                             | 0.00  - 1.00                                                  |
| sat_part_2017     | float64   | SAT     | 2017    | State SAT participation rate for   a given year                                                                                                                         | 0.00  - 1.00                                                  |
| sat_part_2018     | float64   | SAT     | 2018    | State SAT participation rate for   a given year                                                                                                                         | 0.00  - 1.00                                                  |
| sat_part_2019     | float64   | SAT     | 2019    | State SAT participation rate for   a given year                                                                                                                         | 0.00  - 1.00                                                  |
| sat_part_17_to_18 | float64   | SAT     | 2017-18 | Year-on-Year Change in SAT   participation rate. 2018 minus 2017 rates over 2017 rates. Negative refers to   drop in rate YoY while positive means increase in rate YoY | Any positive or negative ratio,   rounded to 3 decimal places |
| sat_part_18_to_19 | float64   | SAT     | 2018-19 | Year-on-Year Change in SAT   participation rate. 2018 minus 2017 rates over 2017 rates. Negative refers to   drop in rate YoY while positive means increase in rate YoY | Any positive or negative ratio,   rounded to 3 decimal places |
| act_part_17_to_18 | float64   | ACT     | 2017-18 | Year-on-Year Change in SAT   participation rate. 2018 minus 2017 rates over 2017 rates. Negative refers to   drop in rate YoY while positive means increase in rate YoY | Any positive or negative ratio,   rounded to 3 decimal places |
| act_part_18_to_19 | float64   | ACT     | 2018-19 | Year-on-Year Change in SAT   participation rate. 2018 minus 2017 rates over 2017 rates. Negative refers to   drop in rate YoY while positive means increase in rate YoY | Any positive or negative ratio,   rounded to 3 decimal places |

## Findings and Recommendations

### Trends in Participation Rate:
There is an uptrend in SAT participation rates between 2017-19. This is a promising outcome - the SAT test format was updated in 2016 to increase its relevance to skills used by students in college and future work settings. 

In general, the ACT participation rates are higher than that of SAT's, but in comparison to SAT, ACT participation rates have been steadily decreasing over the years.

### Relationship between SAT and ACT participation rates
SAT and ACT participation rates are inversely correlated. 

Some states mandate either the SAT or ACT as part of their efforts to monitor student performance. This would definitely skew the preference for one test over the other, and therefore its corresponding participation rate. 

While it is possible for a student to take both the SAT and ACT, it also makes sense to choose and focus on only one given the time and effort required to prep and do well for it. 



#### Opportunities:
While states with low participation rates indicate opportunities for growth, we should also identify areas where competition with ACT is minimised. 
 - We can consider investing into **Alaska** as it has below average participation rates for both SAT and ACT. 

 - Among 10 states with consistently low SAT participation rates (within the first quantile), we can consider growth opportunities in **Iowa** and **South Dakota**. While they do not fall within the first quantile, ACT participation rates in these two states are still relatively lower compared to the others in the same cluster, likely due to the fact that the ACT test is not state-mandated.
 
 - In states where the test is not mandatory, awareness of SAT may be low. We can increase awareness of the SAT (its format, process and function) through education consultancies. We can also offer test fee discounts to attract more test-takers. 

- In states with higher socioeconomic status, ACT participation rates may not necessarily pose as great of a competition to SAT participation rates. This may be due to the fact that students in richer states have the financial means to take multiple tests in the same year. In **Florida**, for example, participation rates for both tests have remained above 50% across 2017-2019. However, as participation rates have been erratic in this state (fluctuating between 56%-100% over 3 years), it may be worthwhile to further study the trends in this state before committing to extensive investments.  

### Relationship between SAT participation rates and average SAT Total Scores
SAT participation rates and average total scores also appear to be inversely correlated. 

This also makes sense:
- In states where the SAT test is not mandatory, only the most motivated and prepared students opt to take the test.
- Conversely, in states where the SAT test is mandatory, students are obligated to sit for the test regardless of their readiness level. Hence, average total scores are lower. 

#### Opportunities:
- In states where the SAT test is not mandatory, we can attempt to improve participation rates by increasing students' morale and motivation to take the test. This can be done by helping to increase their scholastic abilities. For example, we can work with schools to provide more educational support to students through more affordable study materials, or subsidised prep classes. 

- Alternatively, we can collaborate with institutes of higher learning to increase the number of merit scholarships awarded to worthy applicants. While SAT scores are optional for most college admissions, students may be more inclined to take the SAT if it increases their chances of receiving a merit scholarship. 

- Further investigation into SAT section scores can be done to allow us to better refine our strategy. For example, we have identified that the average section scores for both EBRW and Math in **Alaska** are below average. Hence, if we aim to provide educational support to the students in this state, we need to be more holistic in our approach. 

## Conclusion

Strategies to improve SAT participation rates need to consider competition from ACT in the same area. 

In order to elevate SAT participation rates in states where the test is not mandatory, we can motivate students to take the test by boosting their scholastic abilities. Besides providing educational support to students, it may also be worthwhile to engage schools and education agencies to help spread awareness about the SAT and its utility. 


## Sources:

1. https://www.cnbc.com/2019/10/03/rich-students-get-better-sat-scores-heres-why.html

2. https://blog.collegevine.com/here-are-the-average-sat-scores-by-state/
3. https://testive.com/state-sat-act/
4. https://www.crimsoneducation.org/sg/blog/test-prep/sat-vs-act-whats-the-difference/
5. https://sat.ivyglobal.com/new-vs-old


