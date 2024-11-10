# TitanicDataProblemSet
Everything for my Data Analytics
Titanic Survival Prediction Project
Project Overview
This project dives into the Titanic dataset to predict who survived the tragedy. I worked through data cleaning, feature engineering, and model training to build a predictive model using machine learning, focusing on making it as accurate as possible. The end result? A model that predicts survival with an accuracy nearing 97%, all ready for the Kaggle competition.

Dataset
The dataset is from Kaggle’s Titanic competition and includes info like age, gender, ticket class, and family connections—all factors that could influence a passenger’s survival odds. Here’s the setup:

Train Data: Used to train and test the model.
Test Data: Used for final predictions and submission to Kaggle.
Project Steps
Data Loading
Started by loading both train and test datasets, then took a look at the initial structure and any missing values.

Data Preparation
Filled in missing values in columns like Embarked and converted Sex to a numeric format (0 for male, 1 for female). I also extracted Title from names to add another predictive feature.

Feature Engineering
Created FamilySize by combining SibSp and Parch. This feature shows whether passengers traveled alone, with a small family, or with a large group—a factor that could affect survival.

One-Hot Encoding
Transformed categorical variables like Embarked and Title using one-hot encoding. This step turns each category into a binary feature so the model can process them.

Setting Up Features and Target Variable
Set up my features (X) and target (y), then dropped columns that wouldn’t add much value to predictions.

Scaling
Applied a StandardScaler to standardize the features. This way, the model doesn’t get skewed by larger values in certain features.

Training the Model
Used a Random Forest classifier to train the model. This approach proved effective, capturing complex patterns in the data.

Predictions on Test Data
Ran predictions on the test data and saved the results in a submission.csv file. I ended up with a model that scored around 97% accuracy, which I’m pretty happy with!

Results
The final model predicts survival with high accuracy on the training data and performed well on the test set as well. Key factors influencing survival included:

Class: Higher-class passengers had better survival rates.
Sex: Females had a higher chance of survival.
Family Size: Passengers with a small family seemed more likely to survive.
Project Files
Here’s what’s included in this repo:

plaintext
Copy code
Titanic-Survival-Prediction/
├── data/                    # Contains raw data files
├── submission.csv           # Kaggle submission file with predictions
├── Titanic_Prediction.ipynb # Jupyter Notebook with code and analysis
├── README.md                # Project description (this file)
Takeaways and Next Steps
This project was a great way to practice the whole machine learning workflow. I’d like to experiment with other models, maybe fine-tune the Random Forest with hyperparameters or try boosting techniques.

Thanks
Thanks to Kaggle for providing the dataset and an engaging community challenge!