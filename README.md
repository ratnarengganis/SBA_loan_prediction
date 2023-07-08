# SBA Loan Prediction
This project was developed collaboratively as the final assignment of our Data Science Bootcamp, aiming to reduce the default rate of SBA loans using machine learning techniques.

## Problem: 
The Small Business Administration (SBA) is a government agency in the US established to support small businesses. One of its programs involves providing loans to small businesses. However, there is a problem of small businesses defaulting on SBA-guaranteed loans. Since the SBA only guarantees half of the loan, banks suffer losses when small businesses fail to repay.

## Purpose: 
The purpose of this project is to develop a solution to reduce the default rate of SBA loans. By leveraging machine learning techniques and analyzing historical loan data, we aim to build a predictive model that can assess the likelihood of loan default. This model can then be used by banks and lending institutions to make informed decisions and mitigate potential losses.

## Project Workflow
<b>1. Exploratory Data Analysis (EDA)<b> 
<br>
   The first step in the EDA process is to import the SBA Loan Dataset. Descriptive statistic analysis is then performed to gain an initial understanding of the dataset,   including measures such as mean, median, and standard deviation for numerical variables, as well as frequency distributions for categorical variables. The next step involves checking the data types to ensure their appropriateness for each column and examining for the presence of missing values. If any missing values are found, appropriate techniques such as imputation or removal are applied. Lastly, the dataset is limited based on references from journals and official SBA websites, ensuring that the data used aligns with the project's objectives and is sourced from reputable and authoritative references.
   
2. Data Preprocessing
   In the preprocessing phase, several data cleansing steps are performed to ensure the data's quality and suitability for analysis. This includes removing unnecessary symbols or special characters, converting data types as needed, handling missing values through imputation or deletion, addressing duplicated data, and dealing with outliers. Additionally, a crucial step involves transforming the NAICS (North American Industry Classification System) codes into their corresponding industrial sectors to enhance the interpretability of the data. Furthermore, feature transformation techniques are applied to create new variables or modify existing ones to better represent the underlying patterns. Feature encoding is employed to convert categorical variables into a numerical representation suitable for machine learning algorithms. Feature engineering involves deriving new features from the existing ones, aiming to capture more meaningful information for modeling. Lastly, class imbalance is addressed by employing techniques such as oversampling, undersampling, or using algorithms specifically designed to handle imbalanced datasets. These preprocessing steps are crucial for ensuring the data's quality and preparing it for subsequent analysis and modeling stages.
   
3. Modelling
   In the modelling phase, various machine learning algorithms are experimented with to build the predictive models. The methods tested include logistic regression, LightGBM, decision tree, KNN (K-Nearest Neighbors), random forest, and XGBoost. The selection of these methods is based on their suitability for classification tasks and their potential to capture patterns and relationships within the data.

The chosen evaluation metric for model performance is recall. Recall is selected because its objective is to identify potential loan defaults accurately. False positives and false negatives can both have significant impacts on the loss given default, making it crucial to minimize false negatives and increase the number of true positives. By focusing on recall, we aim to prioritize the identification of true defaults, even if it results in some false positives.

After evaluating the models, XGBoost is selected as the final model. It exhibits the highest recall value among all the tested algorithms. This indicates that XGBoost performs better in identifying potential loan defaults compared to the other models. The selection of XGBoost is based on its superior performance in achieving the desired balance between true positives and false negatives, which is essential for accurately predicting loan defaults.

4. Summary and Recommendation:
   Based on the analysis conducted, the two most influential variables in predicting loan defaults are Real Estate and Term. Here are the recommendations for the bank:
   a) For companies that do not have real estate as collateral, both the SBA and the bank should thoroughly examine other financial reports and assess other business assets 
      accurately. This assessment can be used as an additional form of collateral evaluation to provide protection in case the company fails to repay the loan.
   b) Regarding the Term variable, it is recommended to offer long-term loan options with reasonable interest rates. This will provide borrowers with a more manageable 
      payment schedule, increasing the likelihood of loan repayment.
   By implementing these recommendations, the bank can mitigate the risk of loan defaults and make more informed decisions when evaluating loan applications. It is 
   essential to consider a holistic approach that incorporates additional financial assessments and provides flexible repayment options to improve loan repayment rates and 
   minimize financial losses.
