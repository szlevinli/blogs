# Machine Learn Memorandum

## Standardization, Normalization, Regularization

> source: [Differences between Standardization, Regularization, Normalization in ML](https://iq.opengenus.org/standardization-regularization-vs-normalization/)

Key Differences

- Standardization and Normalization are data preprocessing techniques whereas Regularization is used to improve model performance
- In Standardization we subtract by the variable mean and divide by the standard deviation
- In Normalization we subtract by the minimum value divided by the variable range
- In Regularization we tune the function by adding additional penalty term in the error function
- After performing Standardization and Normalization most of the data will lie between a given range,whereas Regularization doesn't affect the data at all
- In Standardization distribution changes to Normal whereas in Normalization and Regularization distribution remains the same
- Standardization must be used when data is normally distributed, Normalization when data is not normal and Regularization when data is very noisy
