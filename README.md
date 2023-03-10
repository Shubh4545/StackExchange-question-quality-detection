# StackExchange question quality detection

# Problem statement
Problem statement given [here](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/70bdf96e0396bd24794deb46ff8337d70dfdb765/StackExchange%20question%20quality%20detection.pdf)

# Goal
Categorise the StackOverflow questions into various quality classes.

# Workflow of project
**Collection of data** 

1.Here we need to extract [data](https://drive.google.com/drive/folders/15xd3v1mSaeGILRnpUUa2V-r2AbGp26kH) from xml file to csv file in correct format/structure. we used **ElementTree** to extract data from xm file. [here](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/847ee6b192ed7aae9ce7fc65141e624eb2f6bd6e/dataset_extraction_code.ipynb) is code for that or run uploaded  data_extraction_code.ipyn file.

2.we need to sample the dataset because dataset is very big so we are using [Simple Random Sampling](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/810a270ad07862bcecc6ba98545006ed4c3c3893/Simple_Random_Sampling.ipynb) or run uploaded Simple_Random_Sampling.ipynb

3.create sample dataset 

we need to create dependent feature based on independent features score and AnswerCount. we are using some conditions which are given in [here](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/bc0173ad10f6be6d2690789875bee4f61f8b82fb/add_dependent_feature.ipynb) or run add_dependent_feature.ipynb

**Data Cleaning**

Clean the data 

**Splitting test and training data**

**Model Training**

**Model Evaluation**

**Prediction System**

