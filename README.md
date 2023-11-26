# Drug reviews sentiment analysis

# Background information

A hospital or insurance provider is interested in efficiently extracting numeric ratings from patients' written review.  To this end we build a model using labelled, numerically, patient reviews. 

Click [here](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugReviews.ipynb) to access full notebook.


# Data exploration



The data comes from Drugs.com and is accessed through UCI's website.


Click [here](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugsComTrain_raw.tsv) to access data. 

![Ratings distribution](https://github.com/jmarksk/DrugReviewAnalysis/blob/main//Images/Ratings distribution.png "y distr")

Ratings are not normally distributed. Counts are highest at the worst and best ratings. 

- 160,000 samples
- 800 unique conditions
- 3400 unique drugs

# Data understanding/preprocessing

- Tokenizing and creating the tf-idf matrix.

# Data modeling

- Baseline Decision Tree model (TF-IDF)

- linear regression (TF-IDF)

- Word embedding models. 


# Results/conclusions

![rmses](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/Images/rmses.png "val rmses")

## Recommendations/future work

- Deployment linear regression (TF-IDF) for ‘rating extraction’ from written review.

- Gather insights on how patients rate drugs.
    - "doctor, love, worse" etc. 
    

- Combine the tf-idf and word embedding models.
- Use the “meta-data” as features. (i.e. the drug evaluated)

## Repository structure
- [Notebook](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugReviews.ipynb)
- README
- [Presentation](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/Presentation.pdf)
- [data](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugsComTrain_raw.tsv)