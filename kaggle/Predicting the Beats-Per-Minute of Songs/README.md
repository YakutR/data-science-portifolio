# Predicting the Beats-per-Minute of Songs | Kaggle
### Playground Serie - Season 5, Episode 9


# Dataset Description
The dataset for this competition (both train and test) was generated from a deep learning model trained on the BPM Prediction Challenge dataset. Feature distributions are close to, but not exactly the same, as the original. Feel free to use the original dataset as part of this competition, both to explore differences as well as to see whether incorporating the original in training improves model performance.

## Files
**train.csv** - the training dataset; BeatsPerMinute is the continuous target ground truth <br>
**test.csv** - the test dataset; your objective is to predict the BeatsPerMinute for each row <br>
**sample_submission.csv** - a sample submission file in the correct format


# Evaluation

Submissions are evaluated using the Root Mean Squared Error between the predicted and the observed target.

## Submission File
For each id in the test set, you must predict a continuous-valued BeatsPerMinute. The file should contain a header and have the following format:

```csv
ID,BeatsPerMinute
524164,119.5
524165,127.42
524166,111.11
etc.
```

# Project Objective

This project has the goal to predict the beats per minute (bpm) of songs, based on the features from a sintect dataset, using machine learning.

## Modeling Strategy

- **Model:** GradientBoostingRegressor
- **Validation techniques:** GridSearchCV, cross-validation
- **Adjusted Hyperparemeters**

# Kaggle Results

- **Public Score:** 26.38950
- **Private Score:** 26.40879

# How to Execute

- Clone the repository
- Install the dependecies: 'pip install -r requirements.txt'
- Execute the notebook in 'src/training'
- Generate the submission file in 'src/'deliver/'submission.csv

# Project Archtecture 

```text
PREDICTING THE BEATS-PER-MINUTE OF SONGS/
├── data/                  # Entry data ('sample_submission.csv','train.csv', 'test.csv')
├── models/                # Fitted-saved models (.pkl)
├── src/
│   ├── analysis/          # EDA´s notebooks
│   ├── training/          # Fitting and validation´s notebooks
│   └── deliver/           # Submission of the final results and graphs
├── README.md              # Project documentation
└── requirements.txt       # List of dependencies
```