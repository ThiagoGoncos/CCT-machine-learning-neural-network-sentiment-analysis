# Machine Learning CA2: Neural Network Regression and Sentiment Analysis

## Project Overview

This project was developed as part of the **Machine Learning for AI** module at **CCT College Dublin**.

The objective of this assessment was to complete two machine learning tasks using Python and Jupyter Notebook:

1. Build and compare regression models, including a Neural Network, to predict visitor spending in London.
2. Perform sentiment analysis on social media text data and visualise the overall sentiment distribution.

The project combines supervised regression modelling, neural network development, data preparation, model evaluation and natural language processing.

---

## Assessment Context

This CA2 assessment was divided into two main parts:

### Part 1: Neural Network Regression

The first part used the `international-visitors-london.csv` dataset.

The target variable was:

```text
Spend (£m)
```

The objective was to predict visitor spending in London using features such as year, quarter, market, duration of stay, mode of transport, purpose of visit, visits and nights.

Because `Spend (£m)` is a continuous numerical value, this part of the project was treated as a supervised regression problem.

---

## Part 2: Semantic / Sentiment Analysis

The second part used text data from social media reviews.

The objective was to classify review text into sentiment categories:

- Positive
- Neutral
- Negative

The sentiment distribution was then visualised and discussed.

---

## Datasets Used

The project uses the following datasets:

```text
international-visitors-london.csv
facebook_reviews.csv
```

### International Visitors London Dataset

This dataset was used for the regression and Neural Network section.

It contains aggregated visitor segment data for London, including:

- year
- quarter
- market
- duration of stay
- mode of transport
- purpose of visit
- area
- visits
- spend
- nights
- sample

Each row represents an aggregated visitor segment rather than one individual visitor.

### Facebook Reviews Dataset

This dataset was used for the sentiment analysis section.

It contains social media review text that was cleaned and analysed to identify overall sentiment.

---

## Part 1: Spend Prediction

The first part of the notebook focused on predicting visitor spending in London.

The main stages included:

- loading the London visitors dataset
- understanding the dataset structure
- checking data types
- checking missing values
- checking duplicated rows
- cleaning inconsistent values
- preparing categorical and numerical variables
- encoding categorical features
- splitting the data into training and testing sets
- scaling data for the Neural Network
- building regression models
- comparing model performance
- making a prediction for a new visitor segment

---

## Data Preparation

The data preparation stage included:

- removing the `area` column because it only contained London
- cleaning the `year` column, including handling `2020P`
- cleaning spacing issues in categorical values
- selecting relevant features for modelling
- encoding categorical variables using one-hot encoding
- preparing scaled and unscaled feature sets
- splitting the dataset into training and testing sets

Scaling was especially important for the Neural Network because neural networks usually perform better when input features are on a similar scale.

---

## Models Implemented

The project implemented and compared the following models:

- Linear Regression
- Random Forest Regressor
- Neural Network Regression using Keras

The models were evaluated using regression metrics including:

- MAE
- MSE
- RMSE
- R² Score

---

## Baseline Regression Results

The initial standard machine learning models produced the following results:

| Model | MAE | MSE | RMSE | R² Score |
|---|---:|---:|---:|---:|
| Linear Regression | 1.8534 | 20.2381 | 4.4987 | 0.6062 |
| Random Forest Regressor | 1.2625 | 13.3895 | 3.6592 | 0.7395 |

Random Forest Regressor performed better than Linear Regression, with lower error values and a higher R² score.

---

## Neural Network Model

A Neural Network regression model was built using TensorFlow / Keras.

The Neural Network used:

- Sequential model structure
- Input layer
- Dense hidden layers
- ReLU activation
- output layer for regression
- Adam optimiser
- Mean Squared Error loss function
- MAE as an additional metric

The baseline Neural Network result was:

| Model | MAE | MSE | RMSE | R² Score |
|---|---:|---:|---:|---:|
| Neural Network Baseline | 1.5346 | 15.2689 | 3.9075 | 0.7029 |

The Neural Network performed better than Linear Regression but did not outperform the Random Forest Regressor.

---

## Model Comparison

The final model comparison showed that Random Forest Regressor was the strongest model overall.

| Model | MAE | MSE | RMSE | R² Score |
|---|---:|---:|---:|---:|
| Random Forest Regressor | 1.2625 | 13.3895 | 3.6592 | 0.7395 |
| Neural Network Baseline | 1.5346 | 15.2689 | 3.9075 | 0.7029 |
| Linear Regression | 1.8534 | 20.2381 | 4.4987 | 0.6062 |

Random Forest was selected because it achieved the lowest RMSE and the highest R² score.

---

## New Visitor Segment Prediction

The final selected model was used to predict `Spend (£m)` for a new visitor segment.

The selected model was:

```text
Random Forest Regressor
```

The predicted value was:

```text
Predicted Spend (£m): 7.16
```

This prediction should be interpreted as the estimated spending for an aggregated visitor segment, not for one individual tourist.

---

## Part 2: Sentiment Analysis

The second part of the project focused on sentiment analysis using Facebook review text.

The main stages included:

- loading the Facebook reviews dataset
- selecting the review text column
- checking and cleaning text values
- preparing text for sentiment analysis
- applying lexicon-based sentiment analysis
- calculating sentiment scores
- assigning sentiment labels
- visualising sentiment distribution
- discussing the results

The sentiment categories used were:

- Positive
- Neutral
- Negative

---

## Sentiment Analysis Method

The project used a lexicon-based sentiment analysis approach.

This means the review text was analysed using known word sentiment values to calculate an overall sentiment score.

Each review was then classified as:

- Positive
- Neutral
- Negative

This approach was suitable because the assessment required a clear sentiment analysis and visualisation of overall positive, neutral and negative sentiment.

---

## Sentiment Analysis Results

The sentiment analysis classified the Facebook reviews as follows:

| Sentiment | Count | Percentage |
|---|---:|---:|
| Positive | 200,580 | 56.38% |
| Neutral | 113,570 | 31.92% |
| Negative | 41,591 | 11.69% |

The results showed that positive sentiment was the most common category in the dataset, followed by neutral sentiment. Negative sentiment represented a smaller proportion of the overall reviews.

---

## Sentiment Visualisation

The notebook includes visualisations showing the distribution of sentiment categories.

The main sentiment visualisation compares:

- Positive reviews
- Neutral reviews
- Negative reviews

This helped make the overall sentiment pattern easier to understand and interpret.

---

## Technologies Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow
- Keras
- Linear Regression
- Random Forest Regressor
- Neural Networks
- VADER Sentiment Analysis
- Natural Language Processing
- Data Visualisation

---

## Project Structure

```text
.
├── ThiagoGoncalves_ML_CA2.ipynb
├── international-visitors-london.csv
├── facebook_reviews.csv
├── Cover Sheet, GItHub Link and References List.docx
├── ML_CA2 v 6.docx
└── README.md
```

---

## Key Learning Outcomes

This project demonstrates understanding of:

- preparing data for regression models
- cleaning and transforming mixed datasets
- encoding categorical variables
- scaling data for Neural Networks
- building standard regression models
- building Neural Network regression models with Keras
- comparing models using MAE, MSE, RMSE and R²
- selecting a final model based on performance
- making predictions on new data
- preparing text data for sentiment analysis
- classifying text as positive, neutral or negative
- visualising sentiment analysis results
- discussing machine learning findings in context

---

## Academic Context

This project was completed as part of the **Machine Learning for AI** module at **CCT College Dublin**.

The work demonstrates both numerical machine learning and text analytics by combining Neural Network regression with sentiment analysis in a single assessment.

---

## Author

This project was developed by **Thiago Goncalves da Costa** as part of the **Bachelor of Science in Computing and Information Technology** at **CCT College Dublin**.

During my studies, I used the institutional GitHub account associated with my student email:

**2022161@student.cct.ie**

Since institutional accounts and student emails may be deactivated after graduation, this repository was migrated to my personal GitHub account:

**https://github.com/ThiagoGoncos**

This ensures long-term preservation of the project, commit history, and academic work completed during the degree program.