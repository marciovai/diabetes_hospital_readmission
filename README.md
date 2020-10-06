## Introduction 
This Notebook was developed based on the [Diabetes 130-US hospitals for years 1999-2008 Data Set](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008#).
The dataset contains clinical data from 130 Us hospitals between 1999 and 2008 collected from patients with Diabetes.  
Here a Data Science pipeline will be developed from Data Exploration to Model Development and Benchmarking.  
Labels contained in the dataset are the following: 

1. No readmission  
2. Readmission in less than 30 days  
3. Readmission in more than 30 days  

Altough for this particular exercise I will make the choice of merging both label items 1 and 3 into a single one, leaving us with a binary classification problem.  

The are two main factors regarding this choice:
- Remove ambiguity from labels: Since labels 2 and 3 are representing fairly similar events. The difference between a patient readmitted 29 days after discharge and one that was readmitted after 31 days will likekly be small. But here they will receive different labels.
- Tackle the main problem: There are many factors that could've influenced a patient to go back to the hospital after more than 30 days have passed, thus it's difficult to tell if the treatment given was the problem. 

So here the objective is to **predict if a patient will be readmitted in a window of 30 days after being discharged**.    

As an additional source of information about the dataset there is [this article](https://www.hindawi.com/journals/bmri/2014/781670/) which explores a bit more on how it was collected and the meaning of each column.
