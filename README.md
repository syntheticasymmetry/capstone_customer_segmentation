# Customer Segmentation Report

## Project Overview
This project addresses two main objectives: creating a **customer segmentation report** and building a **supervised learning model** to predict campaign responses.<br>

By analyzing customer attributes and comparing them with the general population, the project aims to identify key customer segments for a mail-order sales company. This segmentation is then used to inform a predictive model, enablimg targeted marketing efforts.

## Blog Post
For a detailed discussion of the analysis, insights and results of the project, refer to my [blog post here](https://medium.com/@helloworld_2024/customer-segmentation-and-campaign-response-prediction-deef31e35f04).

## Libraries and Tools Used
- Data manipulation: pandas, numpy
- Visualization: matplotlib, seaborn
- Machine Learning: scikit-learn (for PCA, clustering, model training and GridSearchCV)
- Data Preprocessing: SimpleImputer, StandardScaler

## Instructions
1. DOWNLOAD THE DATA: Due to terms and conditions, the csv- and xlsx- files will not be uploaded to the repository. Please download the files separately from [Udacity](https://learn.udacity.com/nanodegrees/nd025/parts/cd1971/lessons/060c9981-1989-486c-b002-f4975ac590de/concepts/241b6561-2146-45e8-ab37-c4566d52e25a?lesson_tab=lesson)
2. SET UP ENVIRONMENT: Install the required Python packages listed in requirements.txt `pip install -r requirements.txt`
3. RUN THE CODE: Data Preprocessing, Customer Segmentation, Model Training and Evaluation, Generate Predictions
4. VIEW RESULTS

## Project structure
- data
    - Udacity_AZDIAS_052018.csv Demographics data for the general population in Germany
    - Udacity_CUSTOMERS_052018.csv Demographics data for established customers of the mail-order company
    - Udacity_MAILOUT_052018_TEST.csv Data from a targeted mail-order campaign, including responses (used for model training)
    - Udacity_MAILOUT_052018_TRAIN.csv (data from a targeted campaign for predictions without labels)
- Arvato Project Workbook.ipynb
- DIAS Attributes - Values 2017.xlsx
- DIAS Information Levels - Attributes 2017.xlsx
- README.md
- requirements.txt
- test_predictions.csv
- gitignore
- test_predictions.csv

## Project Steps and Analysis
1. **Customer Segmentation Report**
This step uses unsupervised learning to explore the attributes of both established customers and general population. The process includes:
- Data Structure Exploration 
- Data Cleaning (handling missing values and scaling features to ensure consistency across datasets)
- Dimensionality Reduction (applying PCA to reduce the number of features while retaining 90% of the variance in the data)
- Clustering (using KMeans clustering to create customer segments, enabling the identification of core customer groups within the population)
2. **Supervised Learning Model**
In this step, the model predicts whether individuals from a mail-order campaign will respond, using insights from the segmentation analysis. Key steps include:
- Model Selection and Initial Training: Logistic Regression was chosen for its interpretability and effectiveness with binary classification.
- Hyperparameter Tuning: GridSearchCV was used to refine parameters, though the final results aligned with the initial model's performance
- Evaluation and Results: The model's predictive accuracy and F1 score were evaluated on a validation set, followed by generating predictions for the test set

## Results Summary
**Customer Segmentation**: Successful identification of customer segments, revealing distinctive attributes of likely customers compared to the general population.<br>
**Prediction Model**: The model demonstrated consistent performance with and without parameter tuning, providing actionable insights into likely campaign responders.<br>
**Further Improvement**: Potential improvements include exploring dataset balancing techniques, such as oversampling or trying alternative models to imrpove the accuracy for the 'Customer' class.

## Acknowledgement
This project was completed as part of a data science course.<br>
Some code components were adapted from my previous project on customer segmentation to meet the specific needs of this project. The corresponding workbook is also uploaded.