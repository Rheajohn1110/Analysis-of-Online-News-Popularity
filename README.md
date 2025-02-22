# Analysis-of-Online-News-Popularity

📌 Project Overview

This project explores the Online News Popularity dataset to analyze factors influencing the popularity of online news articles. We examine article attributes such as content type, publishing details, and audience interactions to uncover patterns that significantly impact readership and sharing behavior.

**Dataset:** • UCI Machine Learning Repository. (n.d.). https://archive.ics.uci.edu/dataset/332/online+news+popularity![image](https://github.com/user-attachments/assets/97181b6e-0cf7-411c-b991-7c2bc0571d8e)


Programming Language: R

# Introduction

The rise of digital media has changed how content is consumed. Understanding what makes an article go viral is valuable for publishers. This project analyzes 39,797 online articles from a publishing platform, identifying key variables that influence sharing behavior.

# Data Exploration & Preprocessing

**Dataset Information**

Total Records: 39,797

Number of Features: 61

Key Variables of Interest

Feature

Description

N_Tokens_Title

Number of words in the title

N_Tokens_Content

Number of words in the article body

N_Unique_Tokens

Rate of unique words in the content

Num_Imgs

Number of images in the article

Num_Videos

Number of videos in the article

Average_Token_Length

Average word length in the content

Data_Channel

Category of the article (e.g., Lifestyle, Business, Tech)

Weekday_Is_

Flags indicating the day of the week the article was published

Is_Weekend

Binary indicator for weekend publications

Shares

Number of times the article was shared

Data Cleaning

Removed duplicate values

Checked for missing values (none found)

Performed descriptive statistics & visualizations

📈 Exploratory Data Analysis (EDA)

🔹 Relationship Between Article Category & Shares

<img width="377" alt="image" src="https://github.com/user-attachments/assets/97e586e1-9c1d-4347-b91b-1b97fe79ad97" />

World Category: Stands out with the highest share counts, indicating viral potential.

🔹 Impact of Publication Day on Shares

<img width="468" alt="image" src="https://github.com/user-attachments/assets/a3956619-7bd1-4366-93d4-6bf8a604eddd" />


Weekdays (Monday - Friday): Higher engagement.

Monday & Wednesday: Peak days for article shares (~20M+ shares).

Weekends: Lower engagement levels.

🔹 Influence of Multimedia Elements (Images & Videos)

Correlation Analysis:

<img width="220" alt="image" src="https://github.com/user-attachments/assets/0126f780-9f4d-4949-81c5-5c3bad2cb266" />


Weak negative correlation (-0.07) between images and videos.

Images (0.02) & Videos (0.04) have minimal impact on shares.

Visual Insights:

Most articles have fewer than 20 images.

No strong trend showing that more images/videos increase shares.

🔹 Effect of Article Length on Popularity

<img width="283" alt="image" src="https://github.com/user-attachments/assets/afbe10c7-e8de-47ef-b1d4-4fc2b1544873" />


Short Articles receive the highest average shares.

Very Long & Long Articles also perform well, while Medium-length articles have lower engagement.

🤖 Predicting Article Popularity Using Machine Learning

📌 Objective

To predict article popularity before publication using historical data.

📊 Model Selection: Support Vector Machine (SVM)

Defined a new binary feature:

Popular (1): Shares > 75th percentile

Not Popular (0): Shares <= 75th percentile

Feature Engineering:

Removed non-numeric & irrelevant features (e.g., URLs, timestamps).

Converted categorical variables into dummy variables.

Train-Test Split: 80% Training, 20% Testing.

Hyperparameters: Cost = 1, Gamma = 0.1.

📈 Model Performance

Metric

Score

Accuracy

95.36%

Confidence Interval (95%)

94.87% - 95.81%

Sensitivity

99.97%

Specificity

81.21%

PPV (Positive Predictive Value)

94.23%

NPV (Negative Predictive Value)

99.87%

🛠️ Key Takeaways:

High Sensitivity: The model effectively detects popular articles.

Lower Specificity: Some misclassification of non-popular articles.

Potential Use: Content strategists can optimize article features for better reach.

Conclusion

This project provides actionable insights into online news popularity. 
Key takeaways:
✅ Weekday Publications Perform Better (Monday & Wednesday are peak days).✅ Short & Very Long Articles Perform Best in terms of engagement.✅ Images & Videos Have Minimal Impact on shares.✅ Machine Learning (SVM) Accurately Predicts Popular Articles with 95% accuracy.

These insights can guide publishers & content strategists in optimizing their articles for maximum engagement and virality.


Explore A/B testing strategies for article optimization.

📖 References

Dataset: UCI Machine Learning Repository
