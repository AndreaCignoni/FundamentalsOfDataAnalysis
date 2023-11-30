<div align="justify"> 

# Tasks: Fundamenentals Of Data Analysis

***

## Task 1: Collatz Conjecture Verification

### Overview

The *Collatz conjecture* is a famous unsolved problem in mathematics stating that a defined function applied to any positive integer **x** will always lead to the repeating sequence $1, 4, 2, 1, 4, 2,1, 2, 3,\ldots$

### Function Definition

The function $f(x)$ is defined as follows:

$ f(x) =
\begin{cases}
x/2 & \text{if } x \text{ is even} \\
3x + 1 & \text{if } x \text{ is odd}
\end{cases}
$gitadd

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




## Jupyter Notebook Implementation

Please feel free to execute my *Jupyter notebook** to view the process and results of the tasks illustrated

### Steps:

1. Open the *Jupyter notebook* using your preferred environment.
2. Run the cells in sequential order to execute the Python code.
3. Review the output and analysis within the notebook to verify the Collatz conjecture.
4. Feel free to explore the code, modify parameters, or adapt it for different ranges as needed.

***

</div>
