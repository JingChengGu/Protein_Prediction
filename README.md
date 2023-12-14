# Protein_Prediction

# Baseline Model <a name="baselinemodel"></a>

- **Description**: In our baseline model, there are 6 predictor features, **'calories'** (quantitative continuous), **'total_fat'** (quantitative continuous), **'sugar'** (quantitative continuous), **'sodium'** (quantitative continuous), **'saturated fat'** (quantitative continuous), and **'carbs'** (quantitative continuous). For this baseline model, we did not have categorical features so no encoding or categorical transformation was done on our given features. We kept our quantitative continuous features as raw integer values. In all, we use 'calories', 'total_fat', 'sugar', 'sodium', 'saturated fat', and 'carbs' as features of our baseline Linear Regression Prediction model.
  
- **Feature Transformations**: We performed the Standard Scaling Transformation to the following features: 'calories', 'total_fat', 'sugar', 'sodium', 'saturated fat', and 'carbs'. The StandardScaler is applied to the specified columns in the ColumnTransformer. Since these features were quantitative features that provide a numerical representation of the nutrition of each recipe, we ensured to subtract the mean value and divide them by the standard deviation of that feature.
  
- **Performance**: The Linear Regression Prediction Model is not great in performance. The primary issue with this model is that it is overly simplistic and tends to make predictions that do not accurately capture the complexity of the data. Specifically, the model appears to predict a similar value for most instances, indicating a lack of variation in different recipe predictions. One approach is to address the class imbalance by either oversampling the minority class (recipes with specific protein counts) or undersampling the majority class (recipes with a more common protein count). Another way to improve our protein prediction is to assign weights to the different protein count classes during model training. By giving higher weights to the minority classes, the model can be encouraged to pay more attention to those classes, potentially improving its predictive accuracy while still using the entire dataset.

- The evaluation metrics are shown below:
<img width="444" alt="Screenshot 2023-12-13 at 4 19 21 PM" src="https://github.com/JingChengGu/Protein_Prediction/assets/64511500/78778385-e955-4051-8503-3a95c4e5782b">
