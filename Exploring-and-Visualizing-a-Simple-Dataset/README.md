# Iris Dataset Exploratory Data Analysis (EDA)

## Project Overview

This project focuses on performing Exploratory Data Analysis (EDA) on the Iris flower dataset using Python visualization libraries. The main objective is to understand the distribution of flower measurements, identify relationships between features, and detect possible outliers.

The Iris dataset is one of the most widely used datasets in data science and machine learning for learning data analysis and visualization techniques.

---

## Problem Statement

Analyze the Iris dataset using visualization techniques to understand feature behavior and relationships among different flower species.

The analysis aims to answer:

* How are the features distributed?
* Which features show clear separation between species?
* Are there any outliers in the dataset?
* Which measurements are most useful for distinguishing flower species?

---

## Dataset

Dataset used: **Iris Dataset**

The dataset contains measurements of Iris flowers from three species.

### Dataset Columns

* **Id** — Unique identifier for each flower sample
* **SepalLengthCm** — Length of sepal in centimeters
* **SepalWidthCm** — Width of sepal in centimeters
* **PetalLengthCm** — Length of petal in centimeters
* **PetalWidthCm** — Width of petal in centimeters
* **Species** — Flower species

### Species

* Iris-setosa
* Iris-versicolor
* Iris-virginica

---

## Objectives

* Load and inspect dataset
* Understand dataset structure
* Visualize feature relationships
* Study feature distributions
* Detect outliers using box plots

---

## Technologies Used

* Python
* Jupyter Notebook
* Pandas
* Matplotlib
* Seaborn

---

## Data Inspection

The dataset was first loaded into a Pandas DataFrame.

Initial inspection included:

* Viewing dataset rows
* Checking column names
* Understanding data structure

Column inspection:

```python
print(df.columns)
```

Output:

```text
Index(['Id', 'SepalLengthCm', 'SepalWidthCm', 'PetalLengthCm',
       'PetalWidthCm', 'Species'],
      dtype='object')
```

The **Id** column was excluded from visualization because it is only a row identifier and does not contribute meaningful analytical information.

---

## Exploratory Data Analysis (EDA)

### 1. Scatter Plot

A scatter plot was created to analyze the relationship between:

* Sepal Length
* Petal Length

Species were represented using different colors.

Purpose:

* Observe clustering
* Understand separation between species
* Identify feature relationships

### Observations

* Iris-setosa forms a clearly separate cluster
* Iris-versicolor and Iris-virginica overlap partially
* Petal length strongly helps distinguish species

---

### 2. Histograms

Histograms were used to analyze the distribution of numerical features.

Features visualized:

* SepalLengthCm
* SepalWidthCm
* PetalLengthCm
* PetalWidthCm

Purpose:

* Study frequency distribution
* Identify common value ranges
* Observe skewness and spread

### Observations

* Petal features show clear grouping
* Sepal measurements overlap more between species
* Petal length and width provide stronger separation

---

### 3. Box Plot

Box plots were created for all numerical features.

Purpose:

* Visualize data spread
* Identify median values
* Detect outliers

The box plot shows:

* Minimum value
* First quartile (Q1)
* Median
* Third quartile (Q3)
* Maximum value
* Outliers

### Observations

* Some outliers were observed in Sepal Width
* Petal measurements show better class separation
* Spread varies across features

---

## Key Insights

From the analysis:

* Petal Length is highly informative
* Petal Width is highly informative
* Sepal Width contains some outliers
* Iris-setosa is easily distinguishable
* Versicolor and Virginica are more similar

---

## Project Workflow

1. Import libraries
2. Load dataset
3. Inspect columns
4. Create scatter plot
5. Create histograms
6. Create box plot
7. Analyze insights

---

## Conclusion

This project demonstrates how Exploratory Data Analysis helps in understanding datasets before machine learning.

By using scatter plots, histograms, and box plots, important relationships and patterns in the Iris dataset were identified. The analysis showed that petal measurements are the most useful features for distinguishing between Iris species.

This project serves as a foundation for future machine learning tasks such as classification and clustering.
