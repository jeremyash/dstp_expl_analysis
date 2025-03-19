
## Beginners Assignment 5: Exploratory Data Analysis

<br><br>


#### **Data:** 

USDA-ERS data on food environment factors (a subset of the Food Environment Atlas), along with county-level food security data from Feeding America. Find the dataset in the assignment folder on the Teams channel [here](https://usdagcc.sharepoint.com/:f:/r/sites/FNS-DataScienceTrainingProgram/Shared%20Documents/FY24-25%20Intermediate/Assignments/Intermediate%20Assignment%203%20-%20Exploratory%20Data%20Analysis?csf=1&web=1&e=7ZvDTm).

This assignment uses the variables listed below.

-   `State` - Name of the state
-   `County` - Name of the county
-   `CHILDPOVRATE15` - Child poverty rate, 2015
-   `PCT_LACCESS_HHNV15` - Percent of households with no car & low access to store, 2015
-   `METRO13` - Metro/nonmetro classification, 2013

For reference, a full list of the variables in this dataset is included at the end of the assignment.

<br><br>


#### **DataCamp:** 

The following DataCamp courses correspond to this exercise:

-   **R**: Exploratory Data Analysis in R, Introduction to Statistics in R, Introduction to Regression in R (bonus question b only)
-   **Python**: Exploratory Data Analysis in Python, Introduction to Statistics in Python, Introduction to Regression with statsmodels in Python (bonus question b only)

<br><br>


#### **Assignment:**

##### *Part A: Load and inspect the data*

1.  Save `EDA_assignment_dataset.csv` to your computer and import the data into a dataframe called `food_env`.
2.  Print the summary statistics for all columns in `food_env`. Do any variables have missing data?
3.  Create a new dataframe named `food_env_full` that excludes rows with any missing data. How many rows were dropped?
<br><br>


##### *Part B: Explore child poverty rates*

4. Plot a histogram of `CHILDPOVRATE15` and add reference lines for the national mean and median. What causes the mean and median to differ?

<br><br>

##### *Part C: Explore low access to stores and no vehicle access*

5.  Plot a histogram of `PCT_LACCESS_HHNV15`. Does it look like the data are skewed? To investigate further, create a boxplot of the `PCT_LACCESS_HHNV15` data.
6. Separate the data into groups by `METRO13`. Make separate histograms where `METRO13` = 0 or `METRO13` = 1. Does `PCT_LACCESS_HHNV15` differ by for metro vs. non-metro areas?
<br><br>


##### *Part D: Exploring relationships*

7. Compute the correlation between `PCT_LACCESS_HHNV15` and `CHILDPOVRATE15`. Then, make a scatterplot with `PCT_LACCESS_HHNV15` on the x-axis and `CHILDPOVRATE15` on the y-axis. 

8. Comment on your results. Do you think the relationship is strong? Are there other factors that could affect both the child poverty rate and a household's access to a grocery store in a county?

9. Is the relationship between `PCT_LACCESS_HHNV15` and `CHILDPOVRATE15` affected by metro status? Separate the data into groups by `METRO13` and repeat step 7 to make scatterplots and calculate the correlation for each group. What might be driving differences shown in these graphs?

<br><br>



##### **Bonus:** 


a. Pick a state. Filter your data down to only that state and recreate the histogram of child poverty rates from step 4. How does it look different to the national graph? Does this make sense, based on what you know about the economy of that state?

b. Return to step 7 and fit a linear regression model where `PCT_LACCESS_HHNV15` is the explanatory variable and `CHILDPOVRATE15` is the response variable. Plot the regression line on the scatterplot. What does this tell you about the relationship between these two variables?

<br><br>


##### **Deliverables:**

-   Your code (the .R, .Rmd, .py, or .ipynb file).
-   These deliverables will be submitted through an MS Form by the end of the program.


<br><br>

##### **Data Dictionary:**

-   `FIPS` - Numeric code that identifies the geographic area
-   `State` - Name of the state
-   `County` - Name of the county
-   `Pop2020` - Population of the county, 2020
-   `POVRATE15` - Poverty rate, 2015
-   `SNAPS17` - Count of SNAP-authorized stores in the county, 2017
-   `CHILDPOVRATE15` - Child poverty rate, 2015
-   `PCT_LACCESS_HHNV15` - Percent of households with no car & low access to store, 2015
-   `GROC16` - Count of grocery stores in the county, 2016
-   `FMRKT_SNAP18` - Count of Farmers' markets that report accepting SNAP, 2018
-   `METRO13` - Metro/nonmetro classification, 2013
-   `food_insecurity_2016` - Food insecurity rate, 2016