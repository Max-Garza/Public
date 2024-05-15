# **DESCRIPTION**
A technical title for a technical project. This file contains code used to test the best way to select words for text mining purposes. Basically, text data is messy, and it's hard to know what words are needed for a proper analysis. This is usually done by removing words that occur less than X% of the time, but I thought there might be a better way - identifying the most important words. So, this file compares the effects of different word selection techniques on text analysis, specifically the categorization of Amazon reviews into specific topics.

## **Files**
* Text_Mining_Sparcity_Reduction.ipynb
  
	Code used to test different word selection techniques.

Data could not be provided due to file size.

## **Use Cases**
Finding the best word selection technique could have many benefits to text mining as it would ensure that models get only the information needed to perform well. Reducing the information that models receive removes multicollinearity issues, speeds up model runtimes, and can improve model performance. In this instance, a good word selection technique means we can better identify the topic of Amazon reviews, but this could improve any number of other text mining operations like IT support ticket classification.

## **Process**
This project is fairly straightforward. I identified one Amazon product, performed basic text preprocessing and topic modeling, and used three word selection techniques:

* Percentage-Based Word Removal
* TF-IDF Word Rankings
* KS-Test Word Rankings
* TF-IDF and KS-Test Mean Rankings
  
Each selection technique was tested with a multinomial Naive-Bayes model, used to classify texts into the topics identified via topic modeling. All techniques were tested at several word counts to see if this made a difference as well.

## **Results**
At least with this dataset, the selection technique used had no effect or a negative effect on model performance when compared to the traditional percentage-based word removal. TF-IDF should be tested further, but the KS-test and the KS+TS-IDF mean rankings proved substantially worse. As of now, there seems to be no reason to deviate from current practices.
