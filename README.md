# IBM-Attrition-Data-Analysis
 What are the demographic, employment, and performance-related factors associated with employee attrition, and how do these factors contribute to the overall attrition rate in the company? Additionally, what insights can be derived from analyzing the dataset to understand the patterns and potential reasons behind employee attrition?

# ----------  Descriptive analysis of the approach adapted to address the problem statement ------------

1. Data loading and exploration:

   - The code starts by importing necessary libraries such as NumPy, Pandas, scikit-learn, Matplotlib, and Seaborn.
   - The dataset is loaded from the file 'IBM Attrition Data.csv' using Pandas ‘read_csv()’ function.
   - The first few rows of the dataset are displayed using the ‘head()’ function to get an overview of the data.
   - Information about the dataset, including column names, data types, and non-null counts, is printed using the `info()’ function.
   - Descriptive statistics of the dataset, such as count, mean, standard deviation, minimum, quartiles, and maximum, are displayed using the `describe()’ function.
   - The code also checks for any missing values in the dataset using the `isnull().sum()’ function.

2. Data visualization:

   - Various data visualizations are performed using Matplotlib and Seaborn to gain insights into the data.
   - Histograms are plotted to visualize the distribution of the 'Age' column and 'Attrition' by age.
   - Count plots are used to visualize 'Attrition' by age group, education, environment satisfaction, job satisfaction, education field, and marital status.
   - These visualizations provide a better understanding of the relationships and patterns in the data.

3. Data preprocessing:

   - The dataset is modified by selecting specific columns of interest using the ‘df[['column1’, 'column2', ...]]’ syntax and assigning it back to the variable ‘df’.
   - The 'Attrition' column is converted from categorical ('Yes' and 'No') to numerical values (1 and 0) using the `replace()’ function.
   - Similarly, other categorical columns such as 'Department', 'EducationField', and 'MaritalStatus' are also converted to numerical representations.

4. Data modeling:

   - The dataset is split into training and testing sets using the `train_test_split()’ function from scikit-learn.
   - The features (x) and target (y) are defined.
   - The features are standardized using the StandardScaler from scikit-learn to ensure all features have the same scale.
   - Logistic Regression is chosen as the classification algorithm/model, and an instance of LogisticRegression is created.
   - The Logistic Regression model is trained on the training data using the ’fit()’ method.
   - The accuracy of the model is evaluated on the training set using the ‘score()’ function.

5. Model evaluation:

   - The trained Logistic Regression model is used to make predictions on the test set using the `predict()` function.
   - The predicted values are stored in the variable ’lr_y_pred’.
   - The predicted probabilities for each class (0 and 1) are obtained using the ‘predict_proba()` function and stored in the variable ‘prob’.
   - The predicted probabilities provide insights into the likelihood of attrition for each employee.

# Overall, this code performs exploratory data analysis, data visualization, data preprocessing, and builds a logistic regression model to predict employee attrition based on various features. The logistic regression model is trained and evaluated using the training and testing datasets, respectively.
