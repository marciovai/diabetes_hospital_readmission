## Introduction 
This Notebook was developed based on the [Diabetes 130-US hospitals for years 1999-2008 Data Set](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008#).
The dataset contains clinical data from 130 Us hospitals collected between 1999 and 2008 from patients with Diabetes.  
The notebook encompasses a pipeline which includes Data Exploration, Model Development and Model Accuracy Analysis.

Labels contained in the dataset are the following: 

1. No readmission  
2. Readmission in less than 30 days  
3. Readmission in more than 30 days  

I have decided to merge the labels 1 and 3 into one, so that the problem becomes a binary classification.

The are two main factors for this choice:
- To remove ambiguity between labels: Since labels 2 and 3 represent the event in which a patient was readmitted. The difference between a patient readmitted 29 days after discharge and one that was readmitted after 31 days will likekly be small, so I've decided to create a single label for both scenarios.
- Tackling the actual problem: There are many factors that could've influenced a patient to go back to the hospital after more than 30 days have passed, thus it's difficult to tell if the treatment given was the ineffective. 

Which lead us to the main objective, **predict whether a patient will be readmitted in a window of 30 days after being discharged**.    

As an additional source of information regarding this dataset there is [this article](https://www.hindawi.com/journals/bmri/2014/781670/) which explores a bit more on how it was collected and the details about each of the features available.
