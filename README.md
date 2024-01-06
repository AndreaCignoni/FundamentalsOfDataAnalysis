<div align="justify"> 

# Assessment Repository

by Andrea Cignoni

***

## Table of Contents

1. [Jupyter Notebook Implementation](#jupyter-notebook-implementation)
    1. [Installation](#installation)
    2. [Usage](#usage)
3. [Part 1: Tasks](#part-1--tasks)
    1. [Task 1: Collatz Conjecture Verification](#task-1-collatz-conjecture-verification)
        1. [Overview](#overview)
        2. [Function Definition](#function-definition)
        3. [Code Development](#code-devolepment)
    2. [Task 2: Overview of the Famous Penguins Dataset](#task-2-overview-of-the-famous-penguins-dataset)
        1. [Overview](#overview-1)
        2. [Dataset Description](#dataset-description)
        3. [Variables Types](#variable-types)
    3. [Task 3: Probability Distribution Modeling for Penguins Dataset Variables](#task-3-probability-distribution-modeling-for-penguins-dataset-variables)
        1. [Overview](#overview-2)
        2. [Variables and Probability Distributions chosen](#variables-and-probability-distributions-chosen)
    4. [Task 4: Probability, Expected Values, Surprise, and Entropy](#task-4-probability-expected-values-surprise-and-entropy)
        1. [Concepts Explained](#concepts-explained)
        2. [Task solution](#task-solution)
    5. [Task 5: Visualization of Palmer Penguin Variables using Seaborn](#task-5-visualization-of-palmer-penguin-variables-using-seaborn)
3. [Part 2 : Project "An Iris Dataset Analysis"](#part-2--project-an-iris-dataset-analysis)
    1. [Introduction](#introduction)
    2. [Dataset Overview: Pandas Exploration](#dataset-overview-pandas-exploration)
    3. [Exploratory Data Analysis: Plotting and Identifying Patterns](#exploratory-data-analysis-plotting-and-identifying-patterns)
    4. [Machine Learning and Flower Species Prediction: Scikit-learn Library](#machine-learning-and-flower-species-prediction-scikit-learn-library)
4. [List Of References](#list-of-references)
    1. [Task 1](#task-1)
    2. [Task 2](#task-2)

***

## Jupyter Notebook Implementation

Please feel free to execute my *Jupyter notebook** to view the process and results of the tasks illustrated

### Installation

1. Clone this repository to your local machine using `git clone`.
2. Navigate to the relevant section or topic you're interested in.

### Usage

1. Open the *Jupyter notebook* using your preferred environment.
2. Run the cells in sequential order to execute the Python code.
3. Review the output and analysis within the notebook to verify the five tasks presented.
4. Feel free to explore the code, modify parameters, or adapt it for different ranges as needed.

***

# Part 1: Tasks

## Task 1: Collatz Conjecture Verification

### Overview

The *Collatz conjecture* is a famous unsolved problem in mathematics stating that a defined function applied to any positive integer **x** will always lead to the repeating sequence $1, 4, 2, 1, 4, 2,1, 2, 3,\ldots$

### Function Definition

The function $f(x)$ is defined as follows:

![!\[image\\](https://github.com/AndreaCignoni/FundamentalsOfDataAnalysis/blob/883d336e071f6d3b79a60383381ce08c091c97e9/img/Formula.png)

### Code devolepment

In order to prove that the *Collatz conjecture* to be true, I have first defined a function *f(x)* implementing the mathematical calculation, then I have created the format how this same function operates in a variable named *collatz()* and, finally, I have encapsulated the iterative process within a loop using a another variable to prove the conjecture's validity for the first 100,000 positive integers. My task was then to verify, using Python, that the *Collatz conjecture* holds true for the first 10,000 positive integers.

## Task 2: Overview of the Famous Penguins Dataset

### Overview

The **Famous Penguins dataset** is a well-known dataset often used in data science and machine learning. It contains information about various penguin species, providing a basis for exploring and understanding the characteristics of these aquatic birds. The raw cvs file was  is downloaded from [mwaskom/seaborn-data Github](https://github.com/mwaskom/) and read using Pandas' **pd.read_csv()** method.

### Dataset Description

The dataset includes the following variables:  **Species**: The species of the penguin: *Adelie*, *Chinstrap*, *Gentoo*; **Island**: The islands where the penguins were observed are *Biscoe*, *Dream*, *Torgersen*; **Bill Length**, **Bill Depth**, **Flipper Length** in millimeters; **Body Mass** in grams; **Sex**: *male* and *female*

### Variable Types

1. **Categorical Variables**

The dataset contains three categorical variables that are *species*, *islands* and *sex* where the first two can be considered as *nominal categorical variables* and the latter  a *nominal variable of the dichotomous type*.

2. **Continuous Variables**

*Bill Length (mm)*, *Bill Depth (mm)*, *Flipper Length (mm)*, *Body Mass (g)* are all continuous variables representing physical characteristics of the penguins. In the data set description, rhey were analysed using Pandas' **describe()** function to provide summary statistics.

## Task 3: Probability Distribution Modeling for Penguins Dataset Variables

### Overview

In Task 3, the assignment consists in selecting an appropriate probability distribution from the **NumPy random distributions list** for modeling each variable in the Famous Penguins dataset.

### Variables and Probability Distributions chosen

**Categorical Variables**

- Species and Island:
The **Multinomial distribution** is suitable for the categorical variables *Species* and *Island,* capturing the probability distribution across multiple categories. 
+ Sex:
The **Binomial distribution** is chosen for the categorical variable *Sex,* which represents a binary outcome.

**Continuous Variables**

* Bill Length, Bill Depth, Flipper Length:
The observed bimodal pattern in the variables suggests the presence of distinct species within the dataset. Given the symmetric spread around the mean, a **Normal distribution** is chosen for modelling the first curve  of the *Bill Length* and both curves for the *Bill Depth* and the *Flipper Length*. The irregular second peak in the *Bill Length* variable is more appropriately modelled by a **Log-normal distribution** due to its specific characteristics.
- Body Mass:
The right-skewed histogram curves with elongated tails on the right side lead to the choice of a **log-normal distribution** for modeling the continuous variable *Body Mass.*

## Task 4: Probability, Expected Values, Surprise, and Entropy

### Concepts Explained

In Task 4, we delve into the concepts of **Probability**, **Expected Values**, **Surprise**, and **Entropy**. These fundamental concepts play a crucial role in understanding the uncertainty associated with random variables and events.

**Entropy** is a measure of the uncertainty or disorder in a set of possible outcomes. It is the expected value of surprise.

Formula:
$H(X) = \sum_{i} P(X=xi) \cdot S(X=xi)$

### Task solution

In the case of flipping two coins, the possible outcomes are 0, 1, or 2 heads. The probabilities for each outcome can be expressed as follows:

Probability of 0 heads: $(1-p)^2$
Probability of 1 head: $2p(1−p)$
Probability of 2 heads: $p2$

The entropy formula is then applied:

$H(X) = -( (1-p)^2 log_2(1-p)^2 + 2p(1-p) log_2(2p(1-p)) + p^2 log_2(p^2) )$

This represents the entropy of the total number of heads when flipping two coins with a probability $p$ of heads. The resulting value would provide a measure of uncertainty or disorder associated with the outcomes.

## Task 5: Visualization of Palmer Penguin Variables using Seaborn

In Task 5, the Palmer penguin dataset was visualised using *Seaborn* to gain insights into the distribution of variables. The following visualizations were created:

- Species Distribution:
A single bar plot using **sns.countplot** was generated for the **Species** variable. The visualisation revealed that the *Adelie* species has the highest representation, followed by *Gentoo*, while *Chinstrap* has the lowest number of samples in the dataset.
+ Species Distribution across Islands:
A bar plot using **sns.countplot** illustrated the distribution of penguin *species* across each island (**Island** variable). The analysis highlighted that the *Adelie* species inhabits all three islands, *Gentoo* is exclusive to *Biscoe* island, and *Chinstrap* is found solely on *Dream* island.
* Sex Distribution across Species:
Another bar plot using **sns.countplot** was employed to visualise the **Sex** distribution across different penguin *species*. The observation indicated almost equal representation of both genders within each species.
- Pair Plot for Continuous Variables:
A pair plot was generated for continuous variables (**bill length**, **bill depth**, **flipper length**, and **body mass**). Distinctions among the three penguin species are more pronounced when each variable is plotted against the common variable of *bill length*.

***

# Part 2 : Project "An Iris Dataset Analysis"

## Introduction

Fisher's Iris Dataset is a well-known dataset in the field of machine learning and statistics, created by the British statistician and biologist Ronald A. Fisher in 1936. It contains measurements of three different species of iris flowers, including **sepal length**, **sepal width**, **petal length**, and **petal width**. This dataset has become a fundamental benchmark for classification and pattern recognition tasks, serving as a foundation for various statistical and machine learning algorithms.  

## Dataset Overview: Pandas Exploration

The analysis starts with an overview of the famous Iris dataset using the Pandas library. This dataset is a popular choice in the field of machine learning and is often used for classification tasks and I have used Pandas to load, analyze, and manipulate the information contained in the CSV file downloaded, gaining insights into its structure and characteristics.

## Exploratory Data Analysis: Plotting and Identifying Patterns

**Entropy Formula for Weak Discrimination**
In the exploratory data analysis phase of the project, I delve into the Iris dataset's features and target variables exploring the concept of entropy as a measure of information gain and use it to understand how well certain features can discriminate between different flower species.

**If Boolean Statements for Linear Discrimination**
To further understand the data, I have implemented conditional statements (if-else) to perform linear discrimination based on selected features. By applying these Boolean statements, it is possible to identify linear boundaries that can help classify Iris flowers into different species.

## Machine Learning and Flower Species Prediction: Scikit-learn Library

In the final phase of the project, I leverage the power of the Scikit-learn library to build machine learning models for flower species prediction.

***

# List of References

## Task 1

[Real Python](https://realpython.com/defining-your-own-python-function/)  

- *Real Python* provides a tutorial on defining custom functions in Python, offering practical insights into function creation and usage.

[Pythontutorial.net](https://www.pythontutorial.net/advanced-python/python-floor-division/)  

- *Pythontutorial.net* explores the concept of floor division in advanced Python, offering a detailed guide on its implementation and significance.

## Task 2

[mwaskom/seaborn-data Github](https://github.com/mwaskom/)  

- The *Palmer Penguin dataset* was downloaded from *GitHub* in raw format and then uploaded in my repository in *csv* format.

[Pandas Official documentation](pandas.pydata.org)  

- The official documentation for Pandas, a powerful data manipulation library in Python, serves as a comprehensive resource for understanding and utilizing Pandas functionalities.

[realpython.com](https://realpython.com/pandas-dataframe/)  

- *Real Python* offers an informative guide on working with Pandas DataFrames, covering various operations and techniques for effective data handling.

[SparkByExamples.com](https://sparkbyexamples.com/pandas/get-pandas-dataframe-shape/)

- *SparkByExamples.com* provides insights into obtaining the shape of a Pandas DataFrame, offering practical examples for data shape exploration.

["A Grahic Primer"](https://mathbench.umd.edu/modules/visualization_graph/page02.htm#:~:text=Scientists%20like%20to%20say%20that,left%20side%2C%20vertical%20one)  

- This resource, titled *"A Graphic Primer,"* provides foundational information on data visualization, emphasizing the importance of graphical representation in scientific contexts.

[Laerd website](https://statistics.laerd.com/statistical-guides/types-of-variable.php/)

- *Laerd*'s website likely provides a guide on different types of variables in statistics, aiding in a better understanding of variables used in data analysis.

### Task 3

[Machine Learning & Simulation YouTube channel](https://www.youtube.com/watch?v=421uW9aZHio)  

- This YouTube channel covers topics related to machine learning and simulation, with the linked video potentially focusing on a specific aspect of these fields.

[ritvikmath YouTube channel]( https://www.youtube.com/watch?v=Dkc_hcVWDpA&t=3s)  

- The *ritvikmath YouTube channel* presents educational content, and the linked video covers a particular topic in mathematics or computer science.

[Analytics Vidhya](https://www.analyticsvidhya.com/blog/2017/09/6-probability-distributions-data-science/)

- *Analytics Vidhya* provides insights into various probability distributions in data science, helping practitioners understand and apply these distributions in their analyses.

### Task 4

[StatQuest with Josh Starmer Youtube channel](https://www.youtube.com/@statquest)  

- The *StatQuest YouTube channel*, hosted by Josh Starmer, is a valuable resource for statistical concepts, offering clear explanations and visualizations for complex topics.

[Entropy (for data science)lecture](https://www.youtube.com/watch?v=YtebGVx-Fxw)

- The linked lecture on entropy, specifically tailored for data science, provides a detailed explanation of entropy's role and applications in the context of data analysis.

### Task 5

[Seaborn official documentation](https://seaborn.pydata.org/generated/seaborn.countplot.html)

- The official documentation for *Seaborn* introduces the countplot function, providing guidance on creating count plots for categorical data visualization using the *Seaborn* library.

### Project

[Towards Data Science](https://towardsdatascience.com/the-iris-dataset-a-little-bit-of-history-and-biology-fb4812f5a7b5)

- This article provides a historical and biological background of the Iris dataset, offering insights into its origins and significance in the field of data science.

[YouTube Iris Dataset EDA Lecture1@ Applied AI Course](https://www.youtube.com/watch?v=FLuqwQgSBDw).

- This lecture proposes an explanatory analysis and interpretation of the dataset offering visual explanations, demonstrations and precious insights.

[archive.ics.uci.edu](https://archive.ics.uci.edu/dataset/53/iris)

- The official dataset repository where the Iris dataset can be found for download, along with detailed documentation.

[pandas.pydata.org](https://pandas.pydata.org)

- The official website for the Pandas library, which is commonly used for data manipulation and analysis in Python.

[scikit-learn official documentation](https://scikit-learn.org/stable/)

- The official documentation for Scikit-learn, a popular Python library for machine learning, including information on how to work with datasets like Iris.

[Shane Lynn](https://www.shanelynn.ie/summarising-aggregation-and-grouping-data-in-python-pandas/)

- A blog post by Shane Lynn that covers summarizing, aggregating, and grouping data using Pandas, which could be relevant for Iris dataset analysis.

[Real Python](https://realpython.com/python-enumerate/)

- Real Python's guide on using the enumerate function in Python, a useful technique for iterating through data.

[CopyProgramming](https://copyprogramming.com/howto/python-matplotlib-ax-set-xticks-size-code-example)

- A tutorial on customizing the appearance of x-axis ticks in Matplotlib, which can be helpful for creating visually appealing plots.

[nickmccullum](https://www.nickmccullum.com/python-visualization/histogram/)

- Nick McCullum's guide on creating histograms in Python, which might be useful for visualizing Iris dataset distributions.

[Analytics Yogi](https://vitalflux.com/python-creating-scatter-plot-with-iris-dataset/)

- A tutorial on creating scatter plots with the Iris dataset in Python, demonstrating data visualization techniques.

[seaborn.pydata.org](https://seaborn.pydata.org/generated/seaborn.pairplot.html)

- The official documentation for Seaborn, a Python data visualization library, including information on creating pair plots with the Iris dataset.

[Scikit-learn: Machine Learning in Python](https://jmlr.csail.mit.edu/papers/v12/pedregosa11a.html), Pedregosa et al., JMLR 12, pp. 2825-2830, 2011

- The academic paper introducing Scikit-learn, providing insights into the library's design and capabilities for machine learning in Python.

***

# End
</div>
