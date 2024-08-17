# Summary / Table of Contents
**- Motivation:** Predict rental prices of homes given simple housing variables (e.g: bedrooms, bathrooms, sq ft, etc.).

**- EDA:** Explored data to gather a feel for the dataset and also to produce cool graphs. 

**- Data Manipulation:** Added a couple variables to assist with our model. Some worked, some didn't, stay tuned to find out. 

**- Model Training:** Trained 3 baseline models. Ended up going with XGBoost regression, used GridSearchCV to tune hyperparameters. Pretty neat stuff.

**- Model Analysis:** Plotted variable importance, reflected on how model can be improved quantitatively and emotionally.

**- Identifying Underperforming Assets:** Discussion on how assets might be identified as "underperforming". Took an income based approach to identify underperforming assets. Learned lots of cool finance concepts like: capitalization rates, DCF. 



## EDA 

<img width="698" alt="Screenshot 2024-08-16 at 15 51 30" src="https://github.com/user-attachments/assets/6b194731-5cb9-48f6-bcf0-70b14741a440">

- The main characteristics of each property are listed in the dataset. However, variables like: school zones, walkability, bikeability are all omitted from the dataset.
- To start my EDA, I wanted to get a sense of the effect each variable had on close price. 

![bedrooms](https://github.com/user-attachments/assets/739ec0f0-671f-473c-afc2-647a11169f1e)

- This is a pretty simple 1 to 1 analysis of bedrooms and how they affect close price. 

![collinearity_beds_baths](https://github.com/user-attachments/assets/5ce43e98-0518-4ed0-8845-670227f11941)

- This is a collinearity analysis of number of bedrooms and number of bathrooms. This analysis was done since I felt these variables were quite closely connected. If there was a high level of collinearity, we can remove of the variables from the model to try to avoid overfitting.
- However, we can see that there is not a terribly high level of collinearity between the two so both variables are included in the model. 

![Geographic](https://github.com/user-attachments/assets/9cb07484-361a-40c1-acee-62806fd40b44)

- The geographical analysis was quite interesting since certain areas are visible within the dataset. Most notably, Florida is visible in the bottom right corner.

## Data Manipulation



![AreaType](https://github.com/user-attachments/assets/59f48dc9-922a-43f2-a2de-58e02b8ddaeb)
