# StackExchange question quality detection

# Problem statement
Problem statement given [here](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/70bdf96e0396bd24794deb46ff8337d70dfdb765/StackExchange%20question%20quality%20detection.pdf)

# Goal
Categorise the StackOverflow questions into various quality classes.

# Workflow of project
**Collection of data** 

1.Here we need to extract [data](https://drive.google.com/drive/folders/15xd3v1mSaeGILRnpUUa2V-r2AbGp26kH) from xml file to csv file in correct format/structure. we used **ElementTree** to extract data from xm file. [here](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/0d064ce6f139447090c017c681e8a0a73b1cc2e7/data_extraction_code.ipynb) is code for that.

2.we need to sample the dataset because dataset is very big so we are using [Simple Random Sampling](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/810a270ad07862bcecc6ba98545006ed4c3c3893/Simple_Random_Sampling.ipynb)

3.create sample dataset 

**Data Preprocessing**

**Splitting test and training data**

**Model Training**

**Model Evaluation**

**Prediction System**

