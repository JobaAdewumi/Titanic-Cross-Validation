# Predict Survival on the RMS Titanic Sinking

## Project Overview
This project predicts the survival of passengers on the RMS Titanic using machine learning techniques. The workflow includes data wrangling, feature engineering, encoding, scaling, model training, and evaluation using the Titanic dataset.

## Author
Adewumi Oluwajoba  

## Dataset
- **File:** Titanic-Dataset.csv
- The dataset contains information about Titanic passengers, including features such as age, sex, fare, class, family size, and port of embarkation.

## Steps Performed

### 1. Data Loading
- Loaded the dataset using pandas.
- Displayed the first 11 rows for initial inspection.

### 2. Data Wrangling
- Checked for missing values.
- Filled missing values in the 'Age' column with the median age.

### 3. Feature Engineering & Encoding
- Converted the 'Sex' column to binary (male: 0, female: 1).
- Created a new feature 'FamilySize' by combining 'SibSp' and 'Parch'.
- Filled missing values in 'Embarked' with the most common port ('S').
- Applied one-hot encoding to the 'Embarked' column.

### 4. Feature Scaling
- Applied Min-Max scaling to 'Age' and 'Fare' columns.

### 5. Model Preparation
- Selected features: Pclass, Sex, Age, Fare, FamilySize, Port_C, Port_Q, Port_S.
- Defined `X` (features) and `y` (target: Survived).

### 6. Model Training & Evaluation
- Split the data into training and test sets (80/20 split).
- Trained a Logistic Regression model.
- Evaluated accuracy on the test set.

### 7. Cross Validation
- Performed 5-fold cross-validation to assess model stability.
- Reported cross-validation scores and average accuracy.

## Requirements
- Python 3.x
- pandas
- scikit-learn

## How to Run
1. Ensure all dependencies are installed:
   ```bash
   pip install pandas scikit-learn
   ```
2. Open and run the notebook `titanic-survival.ipynb` in Jupyter or VS Code.

## Results
- The notebook prints the accuracy of the logistic regression model and the average accuracy from cross-validation.

## File Structure
- Titanic-Dataset.csv: Titanic passenger data
- titanic-survival.ipynb: Main notebook with code and analysis
- README.md: Project documentation (this file)

## License
This project is for educational purposes.
