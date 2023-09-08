# Target-Drug-Administration-Prediction

The objective of this project is to predict, 30 days in advance, whether a patient is eligible to take a "Target Drug." This involves creating a positive set for model development and implementing feature engineering techniques for model building.

## Prerequisites

Before you begin, you will need to have a few tools and libraries installed on your machine:

Python 3.7 or higher.
Sklearn, XGBoost, Pandas

## Data Inferences

- The dataset comprises records for approximately 27,033 unique patients and 57 different types of incidents, spanning over five and a half years.
- The patient with patient_id `a0ddfd2c-1c7c-11ec-876d-16262ee38c7f` was involved in the most number of incidents (1645).
- The most frequent incident recorded was the administration of `DRUG_TYPE_6` (549,616 occurrences).
- The incidents are recorded between `2015-04-07` and `2020-09-03`.

## Workflow

### 1. Project Planning and Understanding

- Brainstormed ideas and devised a plan for tackling the problem statement.
- Gained a comprehensive understanding of the dataset, noting any potential issues such as duplication and inconsistencies.

### 2. Data Preprocessing and Exploration

- Addressed data duplication and index-related issues.
- Explored the dataset by examining unique value counts and descriptive statistics to gain insights.

### 3. Segregating Positive and Negative Sets

- Cleverly separated the incidents related to patients who took the "Target Drug" by considering the 30-day prediction window.
- Merged the segregated set with the original dataset to handle both positive and negative sets effectively.

### 4. Feature Engineering

- Leveraged Pandas groupby(), size(), and unstack() methods to engineer 57 feature columns.
- Created a binary classification target variable by marking patients who had taken the "Target Drug."

### 5. Data Scaling and Balancing

- Addressed data scaling by using a StandardScaler to prepare the data for machine learning algorithms.
- Detected class imbalance and used an Oversampler to address the imbalance issue.

### 6. Model Selection and Tuning

- Explored various machine learning models and selected the GradientBoostingClassifier.
- Performed hyperparameter tuning using GridSearchCV to find the best model parameters.

### 7. Model Evaluation

- Evaluated the model's performance on a validation set and got 80% accuracy with the best possible algorithm and best possible parameters.

### 8. Test Data Prediction

- Processed the test dataset similarly to the training data.
- Used the trained model to predict labels for the test dataset.

### 9. Challenges and Alternative Approaches

- Attempted to improve model performance using PCA and deep learning techniques but with limited success.
- Explained the challenges faced during the model development process in the notebook.


## Future Improvements

- Explore more advanced feature engineering techniques.
- Investigate other machine learning algorithms and deep learning architectures.
- Experiment with different strategies for addressing class imbalance.

## Contact

If you have any questions, comments, or suggestions for the project, please feel free to contact me at [nirmal.works@outlook.com]
