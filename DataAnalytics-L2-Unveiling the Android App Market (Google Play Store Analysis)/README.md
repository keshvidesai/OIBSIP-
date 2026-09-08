# 📱 Android App Market Analysis

## 📌 Project Overview

This project focuses on analyzing the **Android App Market** using a dataset containing information about applications available on the Google Play Store.

The goal is to explore app characteristics, identify trends across categories, analyze ratings and reviews, study pricing and installations, and generate data-driven insights that can help developers understand the Android app market.

The project uses **Python and data analysis/visualization libraries** to clean, analyze, and visualize the dataset.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze the distribution of apps across different categories.
* Identify the most popular app categories.
* Analyze app ratings and reviews.
* Study the relationship between app size, price, ratings, and installations.
* Compare free and paid applications.
* Analyze user sentiment from app reviews.
* Identify categories with the most positive and negative sentiment.
* Visualize important trends and patterns.
* Provide actionable insights for developers planning to launch a new application.

---

## 📊 Dataset

The project uses the **Google Play Store Apps dataset**.

### Dataset Features

Some of the important columns include:

| Column         | Description                    |
| -------------- | ------------------------------ |
| App            | Name of the application        |
| Category       | App category                   |
| Rating         | Average user rating            |
| Reviews        | Number of user reviews         |
| Size           | Size of the application        |
| Installs       | Number of installations        |
| Type           | Free or Paid                   |
| Price          | Application price              |
| Content Rating | Target audience/content rating |
| Genres         | Application genre              |
| Last Updated   | Date of the last update        |
| Current Ver    | Current application version    |
| Android Ver    | Required Android version       |

The dataset contains information about thousands of applications listed on the Google Play Store.

---

## 🛠️ Technologies Used

* **Python**
* **Jupyter Notebook**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical computations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Plotly** – Interactive visualization
* **TextBlob / VADER** – Sentiment analysis

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Univariate Analysis
   ↓
Bivariate & Multivariate Analysis
   ↓
Sentiment Analysis
   ↓
Interactive Visualization
   ↓
Insights & Recommendations
```

---

## 🧹 Data Cleaning

The dataset was cleaned before performing analysis.

Major preprocessing steps include:

* Handling missing values.
* Removing duplicate records.
* Cleaning the `Reviews` column.
* Converting `Installs` into numerical values.
* Removing special characters such as `+` and commas from installation counts.
* Cleaning the `Price` column.
* Converting appropriate columns into numerical/date formats.
* Handling invalid or inconsistent values.
* Checking for outliers where required.

---

## 📈 Exploratory Data Analysis

The project includes several types of visualizations.

### Univariate Analysis

Examples:

* Distribution of app categories.
* Distribution of ratings.
* Free vs paid applications.
* Distribution of installations.
* Content rating distribution.

### Bivariate Analysis

Examples:

* Rating vs number of reviews.
* Price vs installations.
* App size vs rating.
* Category vs average rating.
* Price vs number of reviews.

### Multivariate Analysis

Examples:

* Category, rating, and installations.
* Price, reviews, and ratings.
* App size, installs, and rating.

---

## 💬 Sentiment Analysis

User reviews are analyzed to determine their sentiment.

Reviews are classified into:

* 🟢 **Positive**
* ⚪ **Neutral**
* 🔴 **Negative**

Sentiment analysis helps understand how users feel about applications beyond numerical ratings.

### Sentiment by Category

The project also compares sentiment across different app categories to identify:

* Categories with the highest positive sentiment.
* Categories with the highest negative sentiment.
* Categories with more neutral feedback.

---

## 📊 Interactive Visualization

The project includes at least one interactive visualization using **Plotly**.

Interactive charts allow users to:

* Hover over data points.
* Filter information.
* Explore individual categories.
* Compare different app characteristics.

---

## 🔍 Key Insights

Some of the major insights obtained from the analysis include:

1. **App categories have significantly different levels of popularity and installation counts.**

2. **Free applications generally dominate the Android app market**, making the free-with-monetization model important for developers.

3. **The number of reviews can provide an indication of user engagement and popularity**, although a high number of reviews does not necessarily guarantee a high rating.

4. **User sentiment provides additional information beyond app ratings**, helping developers understand common positive and negative user experiences.

5. **Popular categories can provide opportunities for developers**, but competition should also be considered before launching a new application.

---

## 💡 Recommendations for Developers

Based on the analysis, developers should:

* Research high-demand categories before developing an application.
* Focus on user experience and application quality.
* Monitor user reviews regularly.
* Address recurring negative feedback.
* Optimize application size where possible.
* Consider a free application model with appropriate monetization.
* Analyze competitors before entering a highly competitive category.
* Use user sentiment to identify areas for improvement.

---

## 📁 Project Structure

```text
Android-App-Market-Analysis/
│
├── data/
│   └── googleplaystore.csv
│
├── notebooks/
│   └── android_app_market_analysis.ipynb
│
├── README.md
│
└── requirements.txt
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Navigate to the project folder

```bash
cd Android-App-Market-Analysis
```

### 3. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn plotly textblob vaderSentiment jupyter
```

### 4. Start Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the analysis notebook

Open:

```text
android_app_market_analysis.ipynb
```

Run the cells sequentially to reproduce the analysis and visualizations.

---

## 📦 Requirements

The main Python libraries required are:

```text
pandas
numpy
matplotlib
seaborn
plotly
textblob
vaderSentiment
jupyter
```

---

## 👩‍💻 Author

**Keshvi Desai**

Computer Engineering Student

This project was developed as part of a **Data Analytics / Machine Learning project** to explore the Android application market using real-world data.

---

## ⭐ Conclusion

The Android App Market Analysis project demonstrates how data analytics can be used to understand application-market trends and user behavior.

By combining **data cleaning, exploratory data analysis, visualization, and sentiment analysis**, the project provides useful insights that can support developers in making informed decisions when planning and improving Android applications.

