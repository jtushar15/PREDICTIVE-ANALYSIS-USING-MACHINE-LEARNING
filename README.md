# PREDICTIVE-ANALYSIS-USING-MACHINE-LEARNING TASK-2

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: TUSHAR RAMDAS JADHAV

*INTERN ID*: CT12KEV

*DOMAIN*: DATA ANALYSIS

*DURATION*: 8 WEEKS(January 5th, 2025 to March 5th, 2025.)

*MENTOR*: NEELA SANTOSH

*Rainfall of Australia Country Predictive Analysis | EDA*


Problem Statement:
The main objective of this project is to predict whether or not it will rain in Australia. Rainfall forecast depends on many factors like temperature, humidity, wind speed, wind direction etc.In our project we eant to build a Machine learning Model that can predict whether it will rain or not with maximum accuracy and minimum error.

We impute missing values according to the unique enteries of the Location colun.

:For the numeric column we calculate the median of the column where values are missing by using the unique enteries of the Location column and then fill the missing values with the median. :Same approach is used for the object column.We calculate the mode of the column where values are missing by using the unique enteries of the Location column and then fill the missing values with the mode.

![Image](https://github.com/user-attachments/assets/f90ac564-ea5e-44d1-b372-0bb5d1abae90)

![Image](https://github.com/user-attachments/assets/f84d0de0-0b5d-4849-9a00-8233db3cbdd1)

![Image](https://github.com/user-attachments/assets/d9486381-4a6f-4afe-a198-ca51cc0150d2)

![Image](https://github.com/user-attachments/assets/44dfe17e-48ac-4003-a636-5efb2b26bf31)

![Image](https://github.com/user-attachments/assets/de9d4ded-4719-4592-ae32-b4f5eef55791)

Observation:
Columns like MaxTemp , Rainfall , Evaporation , WindGustSpeed , WindSpeed9am , WindSpeed3pm , Humidity9am , Pressure3pm , Pressure9am , Temp9am , Temp3pm have outliers. Foe dealing these outliers we will use IQR (Interquantile range)

![Image](https://github.com/user-attachments/assets/6f52ad15-7e68-4691-803a-9220391108ce)

Observation:
The outliers have been replaced with median Some columns like Rainfall , Evaporation , WindSpeed3pm have left with extreme values.

![Image](https://github.com/user-attachments/assets/7419690b-00eb-45c3-993b-fe944c5429f4)

![Image](https://github.com/user-attachments/assets/622705d7-f0d3-4a50-8609-9ca054f6e2b8)

![Image](https://github.com/user-attachments/assets/76e50a70-2c07-46a3-94f3-a304c7d6b78b)

Observation:
Some of the columns like MinTemp & MaxTemp shows a higly positive correlation with Temp9am & Temp3pm. As during the day time MinTemp is almost equal to Temp9am and temperature is high during afternoon which means Temp3pm is equal to MaxTemp That's why they shows higly positive correlation. Similarly, Pressure9am and Pressure3pm shows a higly positive correlation. The reason is that atmospheric pressure is remianed almost similar of a placce

![Image](https://github.com/user-attachments/assets/828e8b86-9fce-4328-94b0-4a24bd8fc3e0)

Observations:
Notice how imbalanced is our original dataset! Most of the enteries are with no rain. If we use this dataframe as the base for our predictive models and analysis we might get a lot of errors and our algorithms will probably overfit since it will "assume" that most of time there is no rain. But we don't want our model to assume, we want our model to detect patterns that give signs of rain!

The target variable has class imbalance The value count of RainTomorrow is 0 which means No is 57161 whereas, the count of RainTomorrow = 1 means Yes has only 15705 records.

Hence, to sort this issue we can use oversampling technique SMOTE

![Image](https://github.com/user-attachments/assets/488cc397-2087-4faf-a586-163eeb1444b1)

Observations
Here X is the independent variable and y is the dependent variable which we take both from the resampled data from our indepedent variable for X we drop some higly correlated features like Temp9am, Temp3pm, Pressure3pm Hence, we have to drop one of them to avoid multicollinearity.

Redundant Information: Highly correlated features can provide redundant or similar information to the model, which might not improve predictive performance but could increase computational complexity.

Overfitting: In some cases, highly correlated features can lead to overfitting, where the model learns noise or irrelevant patterns from the data.

![Image](https://github.com/user-attachments/assets/f1a00c97-2b7a-4121-97b7-dcdd20f72656)

# The Best module is Random Forest.
