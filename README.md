<div align="justify"> 

# Tasks: Fundamenentals Of Data Analysis

***

## Task 1: Collatz Conjecture Verification

### Overview

The *Collatz conjecture* is a famous unsolved problem in mathematics stating that a defined function applied to any positive integer **x** will always lead to the repeating sequence $1, 4, 2, 1, 4, 2,1, 2, 3,\ldots$

### Function Definition

The function $f(x)$ is defined as follows:

![image](image.png)

### Example

For instance, starting with an even number, as for instance 10, we divide it by 2 to get 5. Then, as 5 is odd, we multiply by 3 and add 1 to get 16. The same calculation is then repeated dividing by 2 results in the sequence 8, 4, 2, 1. Once at 1, the sequence becomes 4, 2, 1 in a loop.

### Task Requirement

My task was to verify, using Python, that the *Collatz conjecture* holds true for the first 10,000 positive integers.

### Code devolepment

In order to prove that the *Collatz conjecture* to be true, I have first defined a function *f(x)* implementing the mathematical calculation, then I have created the format how this same function operates in a variable named *collatz()* and, finally, I havee ncapsulated the iterative process within a loop using a another variable to prove the conjecture's validity for the first 100,000 positive integers.

## Task 2: Overview of the Famous Penguins Dataset

### Overview

The **Famous Penguins dataset** is a well-known dataset often used in data science and machine learning. It contains information about various penguin species, providing a basis for exploring and understanding the characteristics of these aquatic birds. The raw cvs file was  is downloaded from [mwaskom/seaborn-data Github](https://github.com/mwaskom/) and read using Pandas' **pd.read_csv()** method.

### Dataset Description

The dataset typically includes the following variables:

- **Species**: The species of the penguin: *Adelie*, *Chinstrap*, *Gentoo*.
+ **Island**: The islands where the penguins were observed: *Biscoe*, *Dream*, *Torgersen*.
* **Bill Length (mm)**: The length of the penguin's bill in millimeters.
- **Bill Depth (mm)**: The depth of the penguin's bill in millimeters.
+ **Flipper Length (mm)**: The length of the penguin's flipper in millimeters.
* **Body Mass (g)**: The body mass of the penguin in grams.
- **Sex**: The gender of the penguin: *male* and *female*.

### Variable Types

1. **Categorical Variables**

The dataset contains three categorical variables that are *species*, *islands* and *sex* where the first two can be considered as *nominal categorical variables* and the latter  a *nominal variable of the dichotomous type*.

2. **Continous Variables**

*Bill Length (mm)*, *Bill Depth (mm)*, *Flipper Length (mm)*, *Body Mass (g)* are all continuous variables representing physical characteristics of the penguins. In the data set description, rhey were analyzed using Pandas' **describe()** function to provide summary statistics.

## Task 3: Probability Distribution Modeling for Penguins Dataset Variables

### Overview

In Task 3, the assignment consists in selecting an appropriate probability distribution from the **NumPy random distributions list** for modeling each variable in the Famous Penguins dataset.

### Variable and Probability Distributions chosen

- Species and Island:
The **Multinomial distribution** is suitable for the categorical variables *Species* and *Island,* capturing the probability distribution across multiple categories. 
+ Sex:
The **Binomial distribution** is chosen for the categorical variable *Sex,* which represents a binary outcome.
* Bill Length, Bill Depth, Flipper Length:
The observed bimodal pattern in the variables suggests the presence of distinct species within the dataset. Given the symmetric spread around the mean, a **Normal distribution** is chosen for modeling the first curve  of the *Bill Length* and both curves for the *Bill Depth* and the *Flipper Length*. The irregular second peak in the *Bill Length* variable is more appropriately modeled by a **Log-normal distribution** due to its specific characteristics.
- Body Mass:
The right-skewed histogram curves with elongated tails on the right side lead to the choice of a **log-normal distribution** for modeling the continuous variable *Body Mass.*

### Probability distributions examined

- Categorical variables
**Multinomial distribution** is often utilized with *categorical variables* where an experiment consists of multiple trials, and each trial can result in one of several mutually exclusive outcomes. While a **Binomial distribution** is a discrete probability distribution that models the number of successful outcomes in a fixed number of independent and identical *Bernoulli* trials. The outcome of one trial does not affect the outcome of another trial and the trials are assumed to be independent. 
* Continunous variables
For what concerns the *continuous variables*, the probability distribution considered are the **Normal distribution** and the **Log-normal distribution**. The **Normal distribution**, also known as the *Gaussian distribution* or *bell curve*, is one of the most important and widely used probability distributions in statistics. The *normal distribution* is symmetric, meaning that the left and right sides of the distribution are mirror images of each other and the *mean*, *median*, and *mode* are all located at the center of the distribution. The **Log-normal distribution** is defined for positive real numbers and represents a random variable whose logarithm is normally distributed. Its distribution is typically right-skewed, meaning that the tail on the right side is longer or fatter than the left side.

### Rationale
Probability distributions are used to model variables because they provide a formal and mathematical way to describe and analyze the uncertainty associated with the same variables. Many real-world phenomena, such the measurements contained in the Palmer Penguin dataset, involve inherent randomness or variability and probability distributions provide a model through which it is possible to understand the randomness in data and predict outcomes. The chosen distributions aim to capture the underlying patterns and characteristics of each variable in the dataset.

## Task 4: Probability, Expected Values, Surprise, and Entropy

### Overview

In Task 4, we delve into the concepts of **Probability**, **Expected Values**, **Surprise**, and **Entropy**. These fundamental concepts play a crucial role in understanding the uncertainty associated with random variables and events.

### Concepts Explained

1. Probability
*Probability* is a measure of the likelihood of an event occurring. It ranges from 0 (impossible event) to 1 (certain event). **Probability Distribution** is a mathematical function that specifies the probability associated with different possible values of a variable. The probability distribution is often denoted as $P(X = x)$, where $X$ is the random variable and $x$ represents a specific outcome.

In case of a coin flip the formula is expressed as follows:
$P(\text{Heads})=p$
$P(\text{Tails})=1−p$

2. Expected Values
The *Expected value* of a random variable is a measure of the central tendency of its probability distribution. It represents the average value one would expect to observe over many repetitions of an experiment.

Formula:
$E(X) = sum{x}P(X=x)$

$\Rightarrow$ The *Expected Value* of each outcome is the sum times the probability of observing each outcomes of $x$.

3. Surprise
Surprise measures how unexpected or surprising an event is and it is *the logarithm of the inverse of Probability*.

Formula:
$S(X=xi)=−log2(P(X=xi))$

4. Entropy
Entropy is a measure of the uncertainty or disorder in a set of possible outcomes. It is the expected value of surprise.

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

### Python code implementation

The visual representation of the fenomena discussed has been plotted developping the concepts discussed as follows:

- Probability Values: The probability of getting heads $(p)$ has been defined using the **NumPy linspace function**. The code generates a range of probabilities from a very small positive value (0.00000001) to a very close value to 1 (0.99999999) with fine-grained granularity (1001 values).
+ Entropy Calculation: For each probability $(p)$ in the range, the code calculates the entropy of the total number of heads resulting from two coin flips defining the probabilities of getting 0, 1, or 2 heads and then applying the entropy formula.
* Data Collection: The calculated entropy values for different probabilities are collected in an array.
- Plotting: The **Matplotlib library** is used to plot the entropy values against the corresponding probabilities. The *x-axis* represents the probability of getting heads $(p)$, and the *y-axis* represents the calculated entropy.
+ Visualization: The resulting plot visually illustrates how the entropy of the total number of heads changes as the probability $(p)$ varies.


## Jupyter Notebook Implementation

Please feel free to execute my *Jupyter notebook** to view the process and results of the tasks illustrated

### Steps:

1. Open the *Jupyter notebook* using your preferred environment.
2. Run the cells in sequential order to execute the Python code.
3. Review the output and analysis within the notebook to verify the Collatz conjecture.
4. Feel free to explore the code, modify parameters, or adapt it for different ranges as needed.

***

</div>
