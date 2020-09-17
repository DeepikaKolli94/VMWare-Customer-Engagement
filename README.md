# VMWare-Customer-Engagement
Improving customer engagement at VMWare through Analytics. Data consists of around 600 predictor variables

# Introduction
VMware had various software, cloud and management products; it enabled enterprises to apply a software defined approach to business and IT.They have both digital and non- digital data for their customers and digital data for non-customers. The objective of this project is to analyze the data on customer behavior and provide insights on customer engagement. VMWare Customer Engagement file has the code for the analysis. Dataset - https://store.hbr.org/product/improving-customer-engagement-at-vmware-through-analytics/IMB623

# Technologies
Project is created with R Studio - SMOTE, LiblineaR, ggplot2, randomForest, gbm, xgboost

# Data Analysis & Modeling
1) Handled the null values and necessary conversion of data types in order to process the training data.
2) Data was imbalanced. Target variable had 7 levels where one of the level comprised of 80% of the data. To handle this imbalance in the data we tried over sampling and undersampling using SMOTE. 
3) Data consisted of 700 columns with few redundant columns and rows. Performed exploratory data analysis (EDA) and selected only the significant variables using random forest model and the final cleaned data had about 150 varaiables.
4) With the 150 significant variables, performed Lasso and Ridge with Cross validation and tuned the parameters using recall instead of accuracy as the data was imbalanced. Chose the variables with non zero coefficients fur further analysis and model building.
5) After the feature selection  built various models Random Forest, Regularized Lasso/Ridge, XGBoost to check which performs better on unseen data.

# Results
The variables that are most crucial for the user conversion from visitor to a customer obtained by feature selection are product page views, top resources and pdf downloads, first data of download. Based on various model built, LASSO regression and Gradient Boosting model were giving better recall values and accuracy. Performance of the model can be imprved by understanding the user-behavior of more users. 

With the developed model, there is value addition to the marketing department and the sales department as Marketing department will be able to understand how the company having people at various stages respond to the product and Sales department can contact or can send personalized mails to the companies’ officials regarding the product they may be interested in.
