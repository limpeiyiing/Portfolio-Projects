
# Project 3: Web APIs & NLP 
## Comparing between "Physiotherapy" and "Chiropractic" Subreddits

## Project Statement:

**The client**: An education consultancy who works with prospective undergraduates choosing a college major. The client would like to focus on students wishing to help people with their health, but do not necessarily intend to take up Medicine or Nursing as a major.  

**Task**: Prepare a NLP study of the two topics: "Physiotherapy" and "Chiropractic" based on two Subreddit threads.

**Objectives of the study**:
1) Optimize a classifier model that can successfully categorize unlabelled Subreddit posts into one of the two groups. The best model will be evaluated based on Accuracy and ROC AUC Score. 
2) Compare and contrast between "Physiotherapy" and "Chiropractic" based on model results.

The results of this study will help prospective undergraduates evaluate if either one of these two fields are a good fit with their aspirations.

## Background:
A **physiotherapist/physical therapist**, also known as a PT, focuses on improving your ability to move and function without pain which, in turn, helps boost your quality of life.

The goal of PT is for you to achieve the highest level of movement possible to function in daily life.

PTs evaluate patients and guide them in stretches and exercises, and educate them on ways to stay active and healthy.

**Chiropractors** are licensed professionals with doctorate degrees who use a hands-on approach to ease pain and inflammation by manipulating parts of the body (mainly by adjusting the spine).

The philosophy behind chiropractic care is that the body can heal itself with interventions performed by a chiropractor.

Basically, chiro and physio can treat spinal joint and muscles problem to reduce pain, increase movement and flexibility. Both treat a number of different but similar neuromusculoskeletal conditions including headaches, migraines, back and neck pain, sports injuries, sciatica, scoliosis, disc degeneration. The difference between the two is in the treatment approach.  

**For students interested to pursue either one of these two alternative healthcare professions:** You will need a Bachelor’s Degree or even a Masters to be a Physiotherapist. Chiros are not medical doctors, but graduate with a Doctor of Chiropractic Degree. In the context of Singapore, Physios are employed in both the public and private sector, but chiropractors can only work in a private setting. 

**Sources:** [Healthline](https://www.healthline.com/health/physiotherapist-vs-chiropractor#about-chiropractic-care) and [heal360 PhysioClinic, Singapore](https://physioclinic.sg/physiotherapy-or-chiropractor-in-singapore/)

## The dataset:
The dataset used is a collection of 2742 observations (after cleaning) of Subreddit submissions (SelfText and Titles only, excluding comments) scraped using the Pushshift API. 

About half of this dataset falls under the Physiotherapy category, with posts dated between 7-Jun-21 to 19-Jul-22.

The other half falls under the Chiropractic category, with posts dated between 6-Jan-22 to 19-Jul-22. 

## Findings:

**Best Classification Model:**

- For the time being, among the 7 models tested, the model of choice is the Logistic Regression model coupled to a Count Vectorizer. It has the highest accuracy score, and is rather well balanced across the other performance metrics: specificity, sensitivity, precision and ROC AUC Score.  

- The Logistic Regression model coupled to a TFIDF Vectorizer (Model 3) is the next best choice. It has the same Accuracy as our first choice, but beats it in terms of sensitivity and ROC AUC Score. However, it sacrifices some degree of specificity and sensitivity. 

- As our goal is to correctly classify BOTH classes to retrieve the most amount of correct and useful information for our client, it is equally bad to predict either class incorrectly. In other words, it does not make sense to reduce False Positives or False Negatives in favor of either. Hence, we chose Model 1, which is more well-rounded in terms of performance metrics compared to Model 3. 

**Impact of removing "obvious" words:**:

- Variations of the words "physio" and "chiro" appear as top predictor words in all models. 

- If we remove these "obvious" words from the dataset, performance drops across all metrics. However, the Logistic Regression+Count Vectorizer model is still able to perform rather successfully at classifying posts, with an accuracy of 82% (well-above the baseline score of 51%). 

**Insights:**

- Based on the NLP models created above, we have identified words that set "Physio" apart from "Chiro", mainly: "exercise" (which is more relevant to "physio"), and "adjustment" (which is more relevant to "chiro"). 

- For the purpose of education, we have also discovered that those aspiring to be Physiotherapists need to graduate with a Bachelor's or Master's degree, and pass the PCE (Physiotherapy Competency Examination). On the other hand, those who wish to practice Chiropractic Care need to get a degree in Doctor of Chiropractic. Education options include the Canadian Memorial Chiropractic College (CMCC).


## Future Studies:

It makes sense to further fine-tune model 2 (CVEC+Logistic Regression Model, with variations of the words "physio" or "chiro" removed). This can be done by:

- Scraping extra data to further train the model. Besides referring to Subreddit posts, we can refer to other sources of data related to the two topics (eg: websites of hospitals and physiotherapy/chiropractic clinics)

- Additional Hyperparameter tuning