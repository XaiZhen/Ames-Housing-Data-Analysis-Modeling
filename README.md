# Ames-Housing-Data-Analysis-Modeling

<h2>1.0 Introduction<h2> 
<br>
<h5>House can be considered a necessity for every family or individual, in addition to residential purposes, predicting house price fluctuations and the factors that affect prices can help many real estate agents as well as residential investors make a profit. Therefore, the ability to accurately predict residential property is important for various aspects of society, for example, as mentioned by Rafiei and Adeli (2016), predicting house prices is crucial for near-term economic forecasting in any country.
<br>
<br>
This project examines a data set of sales prices for all residential properties in Ames from 2006 to 2010. The purpose of analyzing this data set is to conduct a model to predict sales prices. The dataset titled "AmeHousing.txt" contains 2.930 observations and 82 variables. In this dataset, the highest sale price for a property is $755,000, and the cheapest is $12,789.
These numerical and categorical variables will be studied in this report, some of these features will be selected to study how these chosen variables can build a best fitted model to predict sale prices<h5>
<br>
<br>

Among the three candidate models provided in this report, the model with the best performance in predicting future residential property prices will be selected through model estimation, model selection and model evaluation.
<br>
<h2>2.0 Candidate Model<h2> 
<h5>All three candidate models used in this report are of the form
<br>
   <p align="center">
<img width="161" alt="image" style="display: block; margin: 0 auto;" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/6ab22972-4218-4d93-83c1-daa774c744d7">
 </p>
  <br>
In this Project Report, y represents the sale price of a property, and the predictor vector, parameter vector and error terms are Xi, βi, and εi. All three proposed model will be discussed more in details in the sub-section under section 2.0.


<br>

<h3> 2.1 Model 1 – M1 <h3> 
   <p align="center">
<img width="431" alt="image" style="display: block; margin: 0 auto;" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/b8059814-d0de-47cf-8ddf-f42e472e1fd0">
 </p>
     <br>
<h5>This function is a multiple linear regression model with two predictor vectors. In model 1, the predictor vectors (xi) selected to predict the sale price are 'Total Bsmt SF' and ‘Gr Liv Area’, as presented in the table above. 'Total Bsmt SF' refers to the basement area in square feet and 'Gr Liv Area’ refers to Above ground living area in square feet. As illustrated in the figure below, there is a strong positive linear relationship between the two features and sales price. The value of zero in feature 'Total Bsmt SF’ will be kept since the overall trend except for x = 0 still shows a positive linear relationship between x and y.
<br>
  <p align="center">
<img width="470" alt="image"  src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/81d4e5b9-4e55-4bcd-b40e-71ae5851dc59">
  </p>
  <br>
  <p align="center">
<img width="470" alt="image"   src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/8d3389bd-4f67-41cc-939a-9d5796261c26">
     </p>
<br>
The reason for choosing these two features in Candidate Model 1 is their relatively high correlation with Sale Price, as indicated in the table and figure in Appendix 1. Further support is given by the fact that in people's domain knowledge, the price of a house is always related to the size of the house. So, in this model, the size of basement and ground floor living area is chosen first for modelling. The model parameters can be estimated from using linear regression functions in ‘sklearn’ packages, values of βi in model 1 is shown in the graph below.
    <br>
<img width="207" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/5a964735-ab60-4473-a3ec-6c5bb1ee9ba8">



</h5>
<br>
<h3> 2.2 Model 2 – M2 <h3>
<p align="center">
<img width="452" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/0e1d5a14-2855-41b8-b7ca-2731195a14e2">
  </p>
<p align="center">
<img width="365" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/789fed11-eb91-452d-941f-5865c219611e">
  </p>

<h5>
This function is a multiple linear regression model with five predictor vectors. Compared with Model 1, three more features have been added while keeping the two features unchanged. X3 is ‘Garage Area’, refers to area of garage, X4 is ‘1st Flr SF’, refers to area of first floor, X5 is ‘2nd Flr SF’, refers to area of second floor. The value of zero in xi will be kept because as the same reasons in Model 1.  As the following figure shows, there is also a strong positive linear relationship between these three features and sales price.

<br>
<p align="center">
<img width="470" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/40e723fb-30fc-4037-80e5-de4b7ee2ba64">
</p>
<p align="center">
<img width="470" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/5b86c91a-eb25-400a-aee4-91644a569df2">
</p>
<p align="center">
<img width="470" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/96eeb8e9-20f9-4059-9f0f-3043a952f2de">
</p>

These three new features were also chosen because they have a linear correlation with Sale price as shown in Appendix 1. Moreover, they are all features that represent the area of different scenes in the house in square feet. Estimation methods of model parameters are same as Model 1, values of βi  is displayed in the graph below.

<img width="192" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/29c1a712-95da-4ab4-92f5-ca97e0720a59">
</h5>


<h3> 2.3 Model 3 – M3 <h3>
  <p align="center">
<img width="624" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/9806d9f9-606d-4219-986c-ff46d0e59c73">
</p>

<h5>
This function is a multiple linear regression model with seven predictor vectors. Two more features have been added in compared with Model 2. In contrast with the other five numerical variables, X6 and X7 are two dummy variables which named ‘PavedRoad_yes’, and ‘Central_Air_yes”, which is created by two nominal variables. ‘PavedRoad_Yes’ refers to whether the road access to property is paved or not paved, value ‘1’ means paved, ‘0’ means not paved and in gravel road condition. ‘Central_Air_yes’ refers to whether central air conditioning is available in property, value ‘1’ means yes and ‘0’ means no. Reasons for choosing the new predictor vectors is because in common sense, in addition to the size of the house, some infrastructure may also be a factor in the price of the house. Hence, these two variables were added to model 3. Values of βi is displayed in the graph below.
<br>
 <img width="172" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/3d1bfa23-ca89-4dd1-b523-d3521e1d31f3">
 
</h5>

<h3> 2.4 Assumptions on the error term in three candidate models <h3>

<h5>
There are four assumptions on the error term in both of three candidate models (Ullah, 2013), which are:
  
1.	Linearity: A linear relationship exists between x and y.<br>
2.	Independence: Errors are independent, which means there is not a relationship between the variables and residuals.<br>
3.	Normality: The error term is normally distributed.<br>
4.	Homoscedasticity: The error terms have equal variance.<br>
And all error terms will be examined in next section.<br>
</h5>

<h2> 3.0 Model Estimation and Selection <h2>

<h3> 3.1 Model Selection Procedure <h3>

<h5>
Validation set approach has been adopted in this process, the available data has been split into a training set, a validation set and a test set (Shah, 2017). As shown in the following figure, the dataset needs to be divided.
<p align="center">
<img width="237" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/569c4cce-0202-48c9-94bc-5e1015bd51d6">
  </p>
<br>
In this project report, all three candidate models follow the rule of randomly dividing 60% of the data into training sets, 20% into validation sets, and the remaining 20% into test sets. In the first stage, the estimation candidate models are generated based on the training set and the estimation results of βi are obtained. Secondly, validation set will be used to predict the observations. Thirdly, the best performing model will be select based on the validation set. Then, the selected model will be re-estimate by combining the training and validation sets.  Finally, predict the observation with the selected model by using test set.


<h3> 3.2 Estimated results of each Candidate Model (based on the training set) <h3>
  <br>
<p align="center">
<img width="588" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/7f22a957-e5eb-46c0-83b1-716862e440ea">
  </p>
<h5>
The estimated results for each candidate model are listed in the table above. It can be observed that the intercept of all three models is negative, and beta 2 is also negative in the values of model 2 and model 3. From this, it can be concluded that if statistical software or statistical code can be used, it is crucial to check the p-value of this predictor vector to examine if it is significant in predicting Y.
  <h5>
 <br>

<h3> 3.3 Examine the assumptions on error terms (residuals) <h3>
<h4> 3.3.1 Model 1 <h4>
 <br>
  <h5>
The verification of the assumptions in Model 1 for the error term is shown in the following combined graph, it can observed that it shows violated linearity, but the q-q plot shows that it is approximately normally distributed, and the squared residuals vs fitted value graphs shows nearly homoskedasticity.
    <h5>
<p align="center">
<img width="350" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/492a7e45-91a4-4f6c-b770-d51e686d6a44">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/557b7860-fac6-4fa6-bf1f-e94cb3fa92b7">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/cdc6bc75-490c-4319-a29b-4ccbcc16548e">
</p>
 <br>
  
<h4> 3.3.2 Model 2 <h4>
<h5>
The verification of the assumptions in Model 2 for the residuals is displayed in the following figures. The verification of the assumptions in Model 2 for the residuals is displayed in the following figures. As similar as the assumption examination in Model 1, the residuals shows non-linearity versus fitted value, assumptions on normality and equal variance satisfied.
  <h5>
<p align="center">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/eb20ff22-4ca2-4a56-93a9-0059458fa40f">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/a52608ae-411b-481f-94cd-116fafeb079e">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/0426a773-79f7-4d7b-9dd5-1887b2341c10">
</p>
  <br>
<h4> 3.3.3 Model 3 <h4>
   
  <br>
  <h5>
From the following plot of Fitted value Vs Residuals it can be noticed that a fairly linear relationship exists between x and y. From the q-q plot it can be found that the residuals are approximately normally distributed, and from fitted values Vs Square Residentials, it can be seen that the residuals have a quite homoskedasticity.
    <h5>
         <br>
<p align="center">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/bae8ae4f-5817-40b4-95ec-dc6c495bb4b1">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/9050e80c-b4b5-4223-ab76-bbb817115856">
<img width="340" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/72cab2c0-efa4-43cf-ad8c-b63ed0097c48">
</p>
  <br>

<h3> 3.4 MSE of each Candidate Model <h3>
<h5>
The following tables shows Mean Square Error (MSE) for each of the Candidate Model. 
<p align="center">
<img width="391" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/8c162fbf-abd5-4bf8-994d-264720addcae">
</p>
     <br>
<h5>
<h3> 3.5 Best Model <h3>
<h5>The best model is Candidate Model 3 since it has the lowest MSE in contrast with other models.<h5>
  <br>

<h3> 3.6 Complexity of the Selected Model <h3>
<h5>
According to Singh (2018), she argues that for models with a few parameters there will be high bias and low variance. Conversely, high variance and low bias would exist for models with a relatively large number of parameters. Of the three candidate models mentioned in this report, Model 3 is the most optimal choice compared to Model 1 and Model 2, it is not too complex or too simple and with lowest MSE.
     <br>
<h5>

<h2>4.0 Model Evaluation <h2> 
     <br>
<h5>
With the candidate model 3 found to be the best model in Section 3.0, it is elected in this section and its performance is re-estimated by combining the training and validation sets to test its performance. 
<br>
However, in this section, the selected model is compared with two benchmark models. The first model predicts the sales price using a constant mean of the sales prices derived from the combined set of the training and validation sets. The second benchmark model uses the average price of the counterpart neighborhood category to predict the sales price of a house. The results obtained in BM1 are based on examining the sales prices in the training and validation sets, and the results obtained in BM2 are based on the test set. The chart below demonstrates the MSE calculated from the three different models, which reveals that the Selected Model has the smallest MSE and is therefore still the best model in this comparison.
     <br>
<p align="center">
<img width="619" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/e42aefce-3321-4177-b7a9-d31449889a79">
</p>
<h5>

<h2>5.0 Conclusion</h2>
  <br>
In conclusion, the Candidate Model 3 has relatively desirable performance in predicting sale prices in contrast with the other two Candidate Models and two Benchmark Models. It exhibits a lower MSE in predictive capability than any of the other four models. Additionally, this project has several limitations and could be improve in the future work. For instance, Model 3 is the one that has most predictor vectors in this project, however, in the actual data set of Ames city house prices, there are 82 variables. If it is necessary to make a superior model for predicting house prices, it is advisable to consider all the features that can be put into the model.


<h2>Reference List</h2>
Rafiei, M. H., & Adeli, H. (2016). A novel machine learning model for estimation of sale prices of real estate units. Journal of Construction Engineering and Management, 142(2). https://doi.org/10.1061/(asce)co.1943-7862.0001047 
<br>
Shah, T. (2017, December 7). About train, validation and test sets in machine learning. towardsdatascience. Retrieved October 25, 2022, from https://towardsdatascience.com/train-validation-and-test-sets-72cb40cba9e7 
<br>
How to train and test data like A pro. SDS Club. (2021, April 4). Retrieved October 27, 2022, from https://sdsclub.com/how-to-train-and-test-data-like-a-pro/  
<br>
Ullah, M. I. (2013, November 3). Assumption about error term archives. Basic Statistics and Data Analysis. Retrieved October 27, 2022, from https://itfeature.com/tag/assumption-about-error-term 
<br>
Singh, S. (2018, May 21). Understanding the bias-variance tradeoff - towards data science. Toward Data Science. Retrieved October 27, 2022, from https://towardsdatascience.com/understanding-the-bias-variance-tradeoff-165e6942b229 
<br>

<h2>Appendix</h2>
<p align="center">
<img width="988" alt="image" src="https://github.com/XaiZhen/Ames-Housing-Data-Analysis-Modeling/assets/157572976/7d896d2d-2e18-4f80-8adb-de38440913d1">
</p>
