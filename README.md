# telecom_2_x_carlos_pinilla
This project analyzes data from a telecommunications company and employs various machine learning models to predict customer churn. It aims to extract insights and support strategic decisions to improve user retention through data-driven approaches.
<span style="color:cyan">

# Index 📋
- Project Description
- Project Access
- Project Stages
- Data Description
- Results and Conclusions
- Technologies Used
- Acknowledgements
- Project Developer

## 1. Project Description 📚
This project involves the development of multiple supervised Machine Learning models aimed at identifying customers prone to churn within a telecommunications company. The model exhibiting the best performance was selected based on specific evaluation metrics.  
Data transformations were applied to meet the requirements of each algorithm, taking into account scale sensitivity and multicollinearity among variables.  
Extensive experiments were conducted within each algorithm family by optimizing hyperparameters, selecting the best performing model per family, and subsequently comparing them. The final selection prioritized the **Recall** metric to minimize false negatives (undetected churners) without significantly compromising Precision, ensuring effective and cost-efficient retention campaigns.  
Finally, a production-like simulation environment was designed with synthetic data to validate model operation using inputs in their original format.

## Project Access 📂
Two options are provided to obtain the project:  
- Clone the repository via command line using:
- Download directly from GitHub at:
#[********************](**********************)  
After downloading, extract the .zip file into the desired directory.

## 3. Project Stages 📝
- Project Description  
- Library Imports and Configurations  
- Data Preprocessing: categorical encoding, normalization, correlation analysis, multicollinearity assessment  
- Data Modeling: train-test split, numerical scaling, dataset balancing  
- Baseline Model (Decision Tree)  
- Advanced Models: Random Forest, Logistic Regression, K-Nearest Neighbors, XGBoost, Support Vector Machine  
- Best Model Evaluation: general metrics, underfitting and overfitting analysis, confusion matrices, feature importances and coefficients  
- Champion Model and Production-like pipeline testing using synthetic data

## 4. Data Description 📊
The dataset integrates pre-cleaned data from prior project stages (7152 observations), including customer records identified as outliers to represent general behavior more faithfully.  
Variables comprise both categorical and numerical types, processed with techniques like one-hot encoding for categorical fields and scaling for numerical fields, with special attention to outliers.

## Class Balance  
Due to imbalance in the target variable ('Churn'), the dataset was downsampled via the NearMiss algorithm to prioritize real data and avoid synthetic bias. This resulted in 3362 training observations, preserving original test data distributions. For production pipeline simulation, synthetic data generated via SMOTENC was used to maintain class distribution fidelity.

## Data Encoding and Scaling  
Different transformations were applied depending on the algorithm family:
- Tree-based models (Random Forest, XGBoost): one-hot encoding with binary variable optimization; numerical variables were not scaled.
- Linear models (Logistic Regression, Linear SVM): one-hot encoding with dropped first category to avoid multicollinearity; numerical variables robustly scaled due to outliers.
- Distance-based model (K-Nearest Neighbors): one-hot encoding with binary optimization; numerical variables scaled similarly.

The response variable ('Churn') was label encoded (`'Yes'` = 1, `'No'` = 0).

## 5. Results and Conclusions ✍️
Models from each family were evaluated and a Champion Model selected for implementation in a simulated production environment. Performance prioritized Recall with threshold adjustments to minimize false negatives, with notable metrics summarized below.  
Random Forest emerged as the Champion Model due to its superior generalization and lowest false positive rate despite some overfitting.

## 6. Technologies Used 🛠️
- Python 3.11.7  
- NumPy  
- Pandas  
- Matplotlib  
- Seaborn  
- Scikit-learn  
- Imbalanced-learn  
- XGBoost  
- Jupyter Notebook  
- Git and GitHub  

## 7. Acknowledgements 🤝
Gratitude is extended to Oracle and Alura LATAM for providing the foundational resources and educational support necessary for this project, enabling the development of future technology talent through their training alliance.

## 8. Project Developer 👷
| Carlos Andres Pinilla | Junior Data Scientist |

</span>
