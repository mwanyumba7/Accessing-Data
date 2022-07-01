# Visual Assessment of Datasets
Visual assessment is simple. It involves looking at your dataset in its entirety in whatever program you like.

Visual assessment can be directed or non-directed.

- **Directed** means looking through each table within a Jupyter notebook or a spreadsheet application like Google Sheets or MS Excel. Unfortunately, some datasets are so large that spreadsheet programs crash when trying to open them, so sometimes *pandas* is the only option.
- **Non-directed** visual assessment is when you look at different pieces of tables, such as scrolling aimlessly and stumbling upon issues, then dialing in on something once you have more of a clue of what issue you've spotted. At that point, you can use more pinpointed assessments whether visual or programmatic.


## 1. Visual Assessment : Acquaint Yourself

Here we will be assessing or data sets visually. 
Firstly you have to acquaint yourself of what the Data Set actually contains and this is well explained in this Practice [Notebook](https://github.com/mwanyumba7/Accessing-Data/blob/main/Visual-Assesment/Acquaint-Yourself/assessing.ipynb) I used for the same.

## 2. Quality : Visual Assessment 1

We now go to the following phase of evaluating the data set's quality using the same Data Set, about which we have a good understanding of what it contains specifically.

Keep in mind that problems with data quality are problems with the content, such as problems with inaccurate data and similar problems.
All three of the tables in this [Notebook](https://github.com/mwanyumba7/Accessing-Data/blob/main/Visual-Assesment/Quality-Assesment_1/quality_assesment_1.ipynb)—the therapy, patient, and adverse reaction tables—will undergo a quality assessment.

[Here](https://github.com/mwanyumba7/Accessing-Data/tree/main/Visual-Assesment/Quality-Assesment_1) are the outcomes of our evaluation of visual quality.

As we do our visual assessment we should keep in mind that this is not Exploratory Data Analysis

**What distinguishes assessing from exploring?**
**Data wrangling** is about:


- **Gathering** the right data
- **Assessing** the data's quality and structure
- **Modifying** the data to make it clean

However, our assessments and modification will not make our analysis, visualizations, or models better. It just makes them work.

**Exploratory Data Analysis (EDA)** is about:


- **Exploring** the data with simple visualizations that summarize the data's main characteristics
- **Augmenting** the data, for example, removing outliers and feature engineering

**Assessing**
In the context of this dataset, **assessing** is everything I just identified [here](https://github.com/mwanyumba7/Accessing-Data/tree/main/Visual-Assesment/Quality-Assesment_1), like spotting:

- Missing HbA1c changes
- Poorly formatted zip codes (e.g., four digits and float data type instead of five digits and string or object data type)
- Multiple state formats (e.g., NY and New York)
- Incorrect patient height values (e.g., 27 inches instead of 72 inches)

**Assessing** is also identifying structural (tidiness) issues that make analysis difficult.
The discovery of these data quality and ensure that the analysis can be executed, which for this clinical trial data includes calculated average patient metrics (e.g. age, weight, height, and BMI) and calculating the confidence interval for the difference in HbA1c change means between Novodra and Auralin patients.

**Exploring**
In the context of this dataset, **exploring** might include using summary statistics like `count` on the state column or `mean` on the weight column to see if patients from certain states or of certain weights are more likely to have diabetes, which we can use to exclude certain patients from the analysis and make it less biased
In the context of a clinical trial, **exploring** is less likely to happen given that clinical trials are expensive and include a lot of pre-planning. So exploring this dataset would likely happen before the clinical trial was conducted.


