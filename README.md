# Regression Model for Property Valuation

## Introduction
The real estate market has experienced significant growth over the years with property valuation increasing by approximately 20% in the past decade due to urbanization. Predicting property values is essential for enabling buyers, sellers, and investors to navigate this complex landscape effectively. Machine learning techniques offer advanced methods for analyzing datasets and uncovering patterns that traditional models may overlook. This project intends to develop various regression model that predicts property values by identifying features importance. The approach involves understanding the features, analyzing their contribution and conducting dimension reduction to ensure the effectiveness of the model.

## Dataset
The dataset analyzed in this project is the House Pricing Dataset which is available on the Kaggle Dataset Repository. It comprises 545 property listing and 13 distinct features representing various property characteristics. Six of these features are numerical variables which are area, bedroom, bathroom, stories, parking and price. Seven of the features is categorical which are furnishing, mainroad, prefarea, guestroom, basement, heating and conditioning. The "furnishing" variable has three possible values which are fully furnished, semi-furnished and not furnished while the other variables are binary and all of these were converted using one hot encoding. The target variable is price and the dataset was split using cross validation.

## Exploration

<p align="center"><img src="https://github.com/user-attachments/assets/0840d79b-0ec9-4a19-8f50-2d4915eb357b" alt="1" style="width: 800px; height: 500px;"></p>

The diagram above displays the scatterplot of area vs price. This helps to visualize the relationship between the two variable and there seems to be a positive correlation as expected. However, there seems to be heteroscedasticity which means that variance in price increase with increase in area.

<p align="center"><img src="https://github.com/user-attachments/assets/eee3359f-dee7-4e91-98e2-34f844e6cc12" alt="2" style="width: 800px; height: 500px;"></p>

The diagram above displays the price distribution in categorical variables. Boxplot shows the number of outliers in the dataset. There is a general increase in mean price with increase in bedroom, bathroom, parking and stories but mean price starts to decrease after certain number.

<p align="center"><img src="https://github.com/user-attachments/assets/22778fb8-1a13-4690-b63d-bfef16a42b4f" alt="3" style="width: 800px; height: 500px;"></p>

The diagram above displays the property number in price range. The shape of the histogram can reveal skewness in the dataset which might effect the model negatively. Most of the houses are in the lower price range which is a reflection of their proportion in the country.

<p align="center"><img src="https://github.com/user-attachments/assets/b5ea69a1-ac52-48bd-ab3c-84bf04db635f" alt="4" style="width: 800px; height: 500px;"></p>

The diagram above displays the distribution of individual binary variables. The barchart displays the number of positive and the number of negative of these features. There is an imbalance in every characteristics and the model will be trained better for the higher number.

<p align="center"><img src="https://github.com/user-attachments/assets/055f544b-db61-415f-8115-3ab40fda3b97" alt="5" style="width: 800px; height: 500px;"></p>

The diagram above displays the correlation between the various features. Features with strong relation can cause overfitting which can cause the model to produce misleading results. This reveals relationship between the target variable price and other individual features.

## Modeling

<p align="center"><img src="https://github.com/user-attachments/assets/79029db3-d37c-479c-8eff-8533260b3891" alt="6" style="width: 800px; height: 500px;"></p>

The diagram above represents the performance score of indivudual models. R-squared measures the proportion of residual between the predicted value and the actual value. The linear regression model performs the best but other model have some useful characteristics.

<p align="center"><img src="https://github.com/user-attachments/assets/18ab12c7-31eb-4115-88df-206fdfa5fbc1" alt="7" style="width: 800px; height: 500px;"></p>

The diagram above represents the importance features for housing price. This analysis was generated based on the random forest model and highlights the features deemed important for predicting housing prices. While area is significantly more influential than other features.

<p align="center"><img src="https://github.com/user-attachments/assets/f949c048-cf0e-4edd-b384-1044cf5a1b77" alt="8" style="width: 800px; height: 500px;"></p>

The diagram above represents the predicted price vs actual price. This visualization shows the accuracy of model in predicting prices with the red line representing ideal predictions. Most points are close to this line which indicates effective pattern capture.

<p align="center"><img src="https://github.com/user-attachments/assets/c481e537-be0c-461c-ad1e-c8037b27a3b1" alt="9" style="width: 800px; height: 500px;"></p>

The diagram above represents the residual analysis of regression model. The scatterplot helps to visualize the nature of the residuals from the prediction. The red line represent zero resudual but most of the points are above suggesting undervaluation by the model.

<p align="center"><img src="https://github.com/user-attachments/assets/321c022b-0077-41e4-9fb3-bdeff8c2dab5" alt="10" style="width: 800px; height: 500px;"></p>

The diagram above represents the learning curve for gradient boosting. The learning curve is essential for regression models as it shows the relationship between training size and performance. The two curves do not meet which mean there is possibility of improvement.

## Conclusion

This project highlights the effectiveness of machine learning models in predicting housing prices which offers stakeholders valuable insights for informed decision-making based on various property features. Utilizing these predictions can help buyers better identify homes within their budget and avoid overpaying for a house. The accuracy of the model could be further improved by incorporating a larger dataset which will allow for a more comprehensive analysis. Additionally, the findings suggest that there are other significant factors influencing prices that have not yet been explored. This presents opportunities for future research to refine the model and enhance its predictive power by integrating additional variables such as neighborhood.
