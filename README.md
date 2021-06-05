# Customer-Churn-Prediction

### Which Domain?
This project aims to solve the churn problem for the banking domain. For any organization or company, customer churn is a major issue.[1] A customer leaving for another product, subscription, or service is a loss for a company. Due to the direct impact on revenue, businesses need to classify customers who are likely to churn and might leave their services in near future. Apart from just recognizing the customers, they also need to identify the reason for churn, to offer them personalized perks. With the help of data mining and machine learning, we can predict the customers at the risk of churning. I am planning to perform two deliverables in this project. First, to predict bank customers likely to churn with the help of supervised learning and customer segmentation using unsupervised learning. There can be many factors causing customer churn, internal and external. In this project, I will try to find the probable reason for churning with the available data.
  
### Which Data?
The source of bank data is Kaggle.[2] This dataset contains details of a bank's customers and the target variable is a binary variable reflecting the fact whether the customer left the bank (closed his account) or he/she continues to be a customer. The dataset contains 10,000 records with 14 columns. There are no missing values. Demographically the information is about customers from Spain, France, and Germany. 55% of customers are Male, and 45% are Female, with an average age of 38.9 years. Exited is the outcome (churn) variable. 
The churn dataset contains below columns - 

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 10000 entries, 0 to 9999
Data columns (total 14 columns):
 #   Column           Non-Null Count  Dtype  
---  ------           --------------  -----  
 0   RowNumber        10000 non-null  int64  
 1   CustomerId       10000 non-null  int64  
 2   Surname          10000 non-null  object 
 3   CreditScore      10000 non-null  int64  
 4   Geography        10000 non-null  object 
 5   Gender           10000 non-null  object 
 6   Age              10000 non-null  int64  
 7   Tenure           10000 non-null  int64  
 8   Balance          10000 non-null  float64
 9   NumOfProducts    10000 non-null  int64  
 10  HasCrCard        10000 non-null  int64  
 11  IsActiveMember   10000 non-null  int64  
 12  EstimatedSalary  10000 non-null  float64
 13  Exited           10000 non-null  int64  
dtypes: float64(2), int64(9), object(3)

Heatmap to find correlation between different variables in the dataset. Exited variable is positively correlated with Age and Balance.


### Research Questions? Benefits? Why analyzes these data?
It is common among many organizations to focus more on attracting new customers rather than retaining the current ones. It could take a serious toll on the company’s revenue and overall profit margins. As per the mixpanel blog post [3], 97% of customers churn silently without providing any explanation. It is tough for a company to keep up with customer churn and make a profit at the same time. The lifetime value of the customer is measured by the total net income of the company from the customer over his lifetime.[6] With churn analysis, we can measure each customer’s value and cost to retain them.  There are many benefits of churn analysis:
-	Increase customer retention.
-	Increase profit margins.
-	Reduce customer attainment expense.
-	Improvement in customer service quality.
-	Lower marketing cost.


### What Method?
	I will start with EDA by exploring summary statistics of data. Planning to do visualization for correlation between variables, exited, vs tenure, gender, age, estimated salary, etc. Based on the analysis, the data will be cleaned and prepared for modeling. Before model implementation, the dataset will be split into test and train sets. 
	For classification, I will be using Scikit-learn [4] K nearest neighbor, Artificial Neural Network, Random Forest, Gradient boosting, and XGB classifier. All the classifiers will be evaluated for their performance. Using sklearn’s [5] GridSearchCV, planning to tune and cross-validate the models. AUC curve will be drawn, to correctly estimate the ability of the model. I will also be testing the model using either precision-recall or ROC curve, depending upon the balancing of the observations. If they are balanced between the class, then ROC will be used, otherwise precision-recall.
	For segmentation, I am planning to use K means clustering by deciding the value of K using the elbow method. 

### Potential Issues?
	The main concern would be the selection of the best method to choose from. For the churn analysis, many approaches can be used, which can provide higher accuracy. Each uses different data structures and has different data selection procedures. Selecting a method with high accuracy and less train time would be the ultimate goal.

### Concluding Remarks
	In the financial and commercial world, machine learning has gotten extensive interest due to its capability of converting raw customer data into useful information.[8] These efforts can easily fail short due to customer churning. So, it is important to focus on customers identified by the churn model. Bank and other financial institutions can greatly benefit from churn analysis. With this research, I will be trying to do customer churn prediction using data mining techniques and gain useful insights from customer’s raw information. 

### References:
1.	What is Churn Analytics? (n.d.). Retrieved from https://mixpanel.com/topics/churn-analytics/ 
2.	Shruti_Iyyer. (2019, April 03). Churn Modelling. Retrieved from https://www.kaggle.com/shrutimechlearn/churn-modelling?select=Churn_Modelling.csv 
3.	97% of users churn silently - here's why. (2020, July 24). Retrieved from https://mixpanel.com/blog/understanding-churn/ 
4.	Pedregosa, F., Varoquaux, G., Gramfort, A., Michel, V., Thirion, B., Grisel, O., ... & Duchesnay, E. (2011). Scikit-learn: Machine learning in Python. the Journal of machine Learning research, 12, 2825-2830.
5.	Sklearn.model_selection.GridSearchCV¶. (n.d.). Retrieved from https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html#sklearn.model_selection.GridSearchCV 
6.	Mutanen, T. (2006). Customer churn analysis–a case study. Journal of Product and Brand Management, 14(1), 4-13.
7.	Prasad, U. D., & Madhavi, S. (2012). Prediction of churn behavior of bank customers using data mining tools. Business Intelligence Journal, 5(1), 96-101.
8.	Kaur, M., Singh, K., & Sharma, N. (2013). Data Mining as a tool to Predict the Churn Behaviour among Indian bank customers. International Journal on Recent and Innovation Trends in Computing and Communication, 1(9), 720-725.
9.	Soeini, R. A., & Rodpysh, K. V. (2012). Applying data mining to insurance customer churn management. International Proceedings of Computer Science and Information Technology, 30, 82-92.
10.	Hashmi, N., Butt, N. A., & Iqbal, M. (2013). Customer churn prediction in telecommunication a decade review and classification. International Journal of Computer Science Issues (IJCSI), 10(5), 271.
