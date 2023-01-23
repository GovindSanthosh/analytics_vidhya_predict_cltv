# analytics_vidhya_predict_cltv
approach for analytics vidhya job-a-thon 2023 january

Claim amount is the only continuous feature. The rest are categorical features. Out of the categorical features, income can be inferred as ordinal.

Policy can also be inferred as ordinal since platinum implies a higher tier of policy than gold and silver and gold implies a higher tier than silver.

Out of these two, rest of the features were converted to numerical using label encoder. Policy and income was converted manually.

Due to high number of categorical variables, linear regression wasn’t used. Both claim amount and  cltv columns are not normally distributed and were unable to make so using box-cox transformation.

Gradient boosting regressor was used to build a model using the train data.
