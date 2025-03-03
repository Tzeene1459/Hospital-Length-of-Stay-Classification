# Hospital Length of Stay Classification

## Project Overview
This project transforms the regression problem of predicting the numerical continuous value of hospital length of stay (`LOS`) into a classification problem. The objective is to classify whether a patient stayed in the hospital for more than a week or not, using Logistic Regression and Random Forest models.

## Classification Approach
We define a binary outcome label:
- **Outcome = 1** if `LOS > 6` days (positive label, longer stay)
- **Outcome = 0** if `LOS <= 6` days (negative label, shorter stay)

The dataset is preprocessed to remove the original `LOS` variable to prevent data leakage. The classification models are then trained and evaluated using precision, recall, and F1-score.

## Tasks Breakdown
1. **Data Loading & Exploratory Data Analysis (EDA)**
   - Load cleaned hospital stay dataset from CSV.
   - Perform initial exploration and visualization.

2. **Feature Engineering & Preprocessing**
   - Create the binary outcome variable `Outcome` based on `LOS`.
   - Ensure correct labeling and verify distribution of `Outcome`.
   - Split the dataset into features (`X`) and target variable (`y`), removing `LOS`.

3. **Train-Test Split**
   - Split data into training and test sets (80% training, 20% testing).
   - Ensure stratification to maintain class balance.

4. **Model Training & Evaluation**
   - Train a Logistic Regression model and evaluate with precision, recall, and F1-score.
   - Train a Random Forest Classifier and compare performance with Logistic Regression.
   - Print classification reports for both models.

5. **Results & Comparison**
   - Analyze the performance differences between Logistic Regression and Random Forest.
   - Assess which model is better suited for predicting longer hospital stays.

## Repository Structure

```
Hospital-Length-of-Stay-Classification
├── README.md            # Project documentation
├── data                 # Data files 
│   ├── los_dataset_cleaned.csv
├── src            # Jupyter Notebooks for analysis
│   ├── LOSModelComparison.ipynb

```

## Usage

### 1. Clone the Repository
```sh
git clone https://github.com/Tzeene1459/Hospital-Length-of-Stay-Classification.git
cd Hospital-Length-of-Stay-Classification
```
Recommended to use colab to install any dependencies through the code. 
Make sure to replace the data path variables with your own. 


## Results Summary
- Logistic Regression and Random Forest achieved **71% accuracy**.
- **Random Forest** performed better in identifying longer stays (higher recall for `Outcome=1`).
- **Logistic Regression** provided more balanced performance across both classes.
- Choice of model depends on whether recall for longer stays or overall balance is prioritized.

## Author 

Tazeen Shaukat

