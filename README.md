### Jonathan Marks, 11/29

# Drug reviews sentiment analysis

# Background information

A hospital or insurance provider is interested in efficiently extracting numeric ratings from patients' written review.  To this end we build a model using labelled, numerically, patient reviews. 

Click [here](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugReviews.ipynb) to access full notebook.


# Data exploration



The data comes from Drugs.com and is accessed through UCI's website.


Click [here](https://archive.ics.uci.edu/dataset/462/drug+review+dataset+drugs+com) to access data. 

Ratings distribution (dependent variable)
![ratingsDistribution](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/Images/ratingsDistribution.png "y distr")

Ratings are not normally distributed. Counts are highest at the worst and best ratings. 

The key columns are the dependent variable, patient numeric rating, and the text review column, the basis for the independent variables.

- 160,000 samples
- 800 unique conditions
- 3400 unique drugs

# Data understanding/preprocessing

- Tokenizing and creating the tf-idf and word-embedding inputs.

# Data modeling

- Baseline Decision Tree model (TF-IDF)

- Linear regression (TF-IDF)

- Word embedding models. 


# Results/conclusions

![rmses](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/Images/rmsesVal.png "val rmses")

## Recommendations/future work/limitations

- Deploy linear regression (TF-IDF) for ‘rating extraction’ from written review, if efficiency reasons dictates that it should be used.  Given the rmse is not very different between the guessing strategy, tested models and chosen models, the results of the model should not be taken blindly. When the stakeholder accumulates written patient reviews without accompanying numerical drug ratings, the stakeholder should use this model to calculate a numeric review so that the drugs can be compared by patient evaluation.  

- Gather general insights on how patients find/rate drugs (i.e. key factors).

    - "doctor, acne, love, worse" etc. 
    -  Words like "doctor" and "acne" can provide us with insight into how a patient will rate the drug that may not be   obvious. 

- Future work
    
    - Create own word embeddings using the whole dataset instead of using Glove. 
    - Combine the tf-idf and word embedding models.
    - Use the “meta-data” as features. (i.e. the drug evaluated)

- Limitations

    - Given the rmse is not very different between the guessing strategy, tested models and chosen models, the results of the model should not be taken blindly.
    - There is material difference between the chosen model's prediction and the actual ratings
    - There may be less clarity when using nlp techniques in understanding what the model (and coefficients) mean. 
    

## Repository structure
- [Notebook](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugReviews.ipynb)
- README
- [Presentation](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/Presentation.pdf)
- [data](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/drugsComTrain_raw.tsv)
- [CodingEnvt](https://github.com/jmarksk/DrugReviewAnalysis/blob/main/CodingEnvt.txt)