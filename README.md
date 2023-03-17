# StackExchange question quality detection

# Problem statement
Problem statement given [here](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/70bdf96e0396bd24794deb46ff8337d70dfdb765/StackExchange%20question%20quality%20detection.pdf)

# Goal
Categorise the StackOverflow questions into various quality classes.

# Workflow of project
## **1.Collection of data** 

1.Here we need to extract [data](https://drive.google.com/drive/folders/15xd3v1mSaeGILRnpUUa2V-r2AbGp26kH) from xml file to csv file in correct format/structure. we used **ElementTree** to extract data from xm file. 

2.we need to sample the dataset because dataset is very big so we are using Simple Random Sampling

3.create sample dataset 

we need to create dependent feature based on independent features score and AnswerCount. we are using some conditions which are given in problem pdf 

## **2.Data Cleaning**

2.1 During Cleaning i removed unwanted columns like ['Unnamed: 0','Unnamed: 0.1','Id','PostTypeId','AcceptedAnswerId','AnswerCount','Score']

2.2 Data['Body'] contains unwanted tags we removed it

2.3 we converted Body and Title feature from text to length of Text.

2.4 i observed data contains outlires but in this dataset context we are not removing it 

## **3.EDA**

3.1 Observed dataset is distributed inbalanced way

![inbalanced](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/2fcfd6fd68b6511b5034ededd20ef77b3b68c747/Resource/inbalalenced.png)

3.2 In dataset body_text_length is distribute normally other features are skewed positive

![body_text_length](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/f8e472eadb056d6c535593df6c92c9e3f731d6dd/Resource/body_text_length.png)

3.3 View_Count have high Correlation 

![corr](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/8c81805f0501012b1eebd650d786d74d4dc17670/Resource/corr.png)

## **4.Splitting test and training data**


**5.Model Training**
5.1 we have trained logistic regression,Random Forest and Multinomial Naive Bayes
and results are

![result](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/49759e144079cf5ac1878d23e17960c7a48a8717/Resource/scores%20table.png)

5.2 Feature Importance

Most Important feature is View_Count 

![Feature](https://github.com/Shubh4545/StackExchange-question-quality-detection/blob/95591f43b91f2a9b1f918ad9df2c2f535963fe58/Resource/Feature%20importance.png)
## **5.Conclusion**
Based on the evaluation of the three models (Random Forest, Logistic Regression, and Multinomial Naive Bayes), the following conclusions can be drawn:

Random Forest has the highest train accuracy of 100% but slightly lower test accuracy of 83.12%. However, it has excellent precision, recall, and F1-scores on both train and test sets, indicating that it is a reliable model for classification tasks.

Logistic Regression has a slightly lower train accuracy of 83.45% but similar test accuracy of 83.53%. Its precision, recall, and F1-scores are also reasonable, indicating that it is a good alternative to the Random Forest model.

Multinomial Naive Bayes with SMOTE has the lowest test accuracy of 70.87% and lower precision, recall, and F1-scores than the other models. Therefore, it is not a recommended model for this classification task.

Overall, based on the evaluation metrics, Random Forest and Logistic Regression are both good models to consider for this project, but Random Forest may be a slightly better option due to its higher train accuracy. However, it is important to also consider other factors such as computational efficiency and interpretability when making a final decision on the model to use.

## **6.Future Work**

Domain-specific Pre-processing: Pre-processing can be customized according to domain-specific knowledge. For example, if the task is to classify the question based on score and AnswerCount is still not perfect we can improve there

