# CourseraAI
Tugas Coursera
✅ Project Goal
Your task is to build a machine learning model using data from accelerometers on the belt, forearm, arm, and dumbbell to predict the "classe" variable, which indicates the manner in which an exercise was performed.

🛠️ Recommended Project Workflow (for your R Markdown report)
1. Load and Clean the Data
Load the training and test datasets.

Remove variables with too many missing values (NA, empty strings).

Eliminate near-zero variance predictors and irrelevant columns (e.g., timestamps, row numbers).

Convert the response variable (classe) to a factor.

2. Partition the Training Data
Use caret::createDataPartition() to split the training data into:

Training set (e.g., 70%)

Validation set (e.g., 30%) for estimating out-of-sample error

3. Feature Engineering (if any)
Optional: PCA or other dimensionality reduction if you want to manage high dimensionality.

4. Train Multiple Models
Use cross-validation (e.g., 5- or 10-fold CV) to compare models. Recommended options:

Random Forest (method = "rf")

Gradient Boosting Machine (gbm)

Support Vector Machine (svmRadial)

Decision Trees (rpart for baseline)

Use caret::train() to streamline model training with resampling and tuning.

5. Evaluate Model Performance
Use accuracy, confusion matrix, and kappa statistic.

Report cross-validation results.

Choose the best-performing model based on expected out-of-sample error on the validation set.

6. Final Model and Predictions
Retrain your final model on the full training dataset (after cross-validation).

Use it to predict the 20-class test set (pml-testing.csv).

7. Prepare Submission
Output your predictions in the required format for the Course Project Prediction Quiz.

Generate the compiled HTML file using knitr::knit2html() or similar.

Host your GitHub repo with the .Rmd and .html files, ideally using a gh-pages branch.

📊 Structure of the R Markdown Report
Your report should include the following sections:

Introduction

State the problem and the importance of quantifying how well the activity is performed.

Data Cleaning and Preprocessing

Describe variable selection, missing data handling, etc.

Model Selection and Cross-Validation

Compare models and explain your selection.

Out-of-Sample Error Estimate

Report validation accuracy and expected generalization performance.

Final Predictions

Include results and note the consistency across cross-validation folds.

Conclusion

Justify modeling decisions and reflect on limitations or future work.

✅ Submission Checklist
 R Markdown (.Rmd) file with full analysis

 Compiled HTML file

 Hosted on GitHub with a shareable repo link

 gh-pages branch enabled (optional but recommended)

 Predictions for 20 test cases submitted to the quiz system
