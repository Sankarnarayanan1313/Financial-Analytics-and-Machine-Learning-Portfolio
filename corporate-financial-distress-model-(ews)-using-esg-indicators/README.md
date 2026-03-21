# corporate-financial-distress-model-(ews) Using ESG Indicators

### Project Overview

**Goal** - Develop a binary risk classification model using ESG (Environmental, Social, Governance) indicators to predict financial distress as defined by the Altman Z-Score.
purpose of this model is to identify whether a ESG data can act as a warining risk signal indicator

 - **1**. We will Define the Target Variable (Altman Z-Score) and classify companies into two categories based on their scores. For the Model i choose thershold of**1.8** as the cutoff for Distress and above are Safe Zone. [Disclaimer - Reason for binary classificaton is to simplify the model and focus on identifying companies at risk and since we don't have a more data to define more multi class model, i will be using binary classification for this project to avoid bias between class]

 - **2** We will use two models - Logistic Regression as base model and XGBoost as  to predict the risk of financial distress based on ESG data.

 - **3**. We will interpret the results of the models to understand which ESG factors are most influential in predicting financial distress. 

1. **Global Target Alignment & Financial Strength**  
   As per the model, firms aligned with global targets and having higher financial strength(Piotroski Score) show a higher probability of being in the Safe zone. This could be a combination of possible regulatory support and increased reputation due to company commitments towards net zero.

2. **Tobacco and Alcoholic Beverages Involvement**  
   Tobacco involvement and Alcoholic Beverages is in lower probability of being in Distress Zone, which could be due to higher cash flow and margins of these industries. Overall, they appear financially stable and profitable.

3. **Temperature Alignment**  
   companies that are aligned with temperature targets show a moderate distress signal, could be due to spending on transition(Risk) towards net zero.

4. **ESG Controversies & Weapons Involvement**  
   ESG controversies and involvement in weapons act as distress signals for companies, possibly due to regulatory pressure or reputational damage.

5. **Gambling Involvement**  
   Involvement in gambling shows a strong distress signal for companies. Major reasons could include regulatory restrictions, operational limitations in certain regions, and potential reputational damage causing companies to fall into severe categories.

# Model Limitations and Own Conclusions

### Data Nature and Limitations

 - The target variable is the Altman Z-Score, which measures bankruptcy risk. However, the dataset does not contain strong financial variables directly linked to the Altman components. As a result, the model performance is limited and works only within the scope of the available ESG and related features.

 - Despite limited information, the model was able to capture meaningful relationships and giving economically meaningful insights. The results suggest that ESG features and the Piotroski score may indirectly influence or relate to the Altman score, providing moderate predictive insight into financial distress.

**Dataset information** The dataset was obtained from Kaggle and around 2 years old. the model output and its meaning are not representing the current trends.
