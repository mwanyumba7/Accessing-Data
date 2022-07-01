# Visual Assessment of Datasets
Visual assessment is simple. It involves looking at your dataset in its entirety in whatever program you like.

Visual assessment can be directed or non-directed.

- **Directed** means looking through each table within a Jupyter notebook or a spreadsheet application like Google Sheets or MS Excel. Unfortunately, some datasets are so large that spreadsheet programs crash when trying to open them, so sometimes *pandas* is the only option.
- **Non-directed** visual assessment is when you look at different pieces of tables, such as scrolling aimlessly and stumbling upon issues, then dialing in on something once you have more of a clue of what issue you've spotted. At that point, you can use more pinpointed assessments whether visual or programmatic.


## Data Quality Dimensions 

Data quality dimensions help guide your thought process while assessing and also cleaning. The four main data quality dimensions are:


1. **Completeness**: do we have all of the records that we should? Do we have missing records or not? Are there specific rows, columns, or cells missing?
2. **Validity**: we have the records, but they're not valid, i.e., they don't conform to a defined schema. A schema is a defined set of rules for data. These rules can be real-world constraints (e.g. negative height is impossible) and table-specific constraints (e.g. unique key constraints in tables).
3. **Accuracy**: inaccurate data is wrong data that is valid. It adheres to the defined schema, but it is still incorrect. Example: a patient's weight that is 5 lbs too heavy because the scale was faulty.
4. **Consistency**: inconsistent data is both valid and accurate, but there are multiple *correct* ways of referring to the same thing. Consistency, i.e., a standard format, in columns that represent the same data across tables and/or within tables is desired.

Regarding the other data quality research, there exists additional dimensions that are specific cases of these four dimensions listed above. Example: currency, defined as follows: the degree to which data is current with the world that it models. Currency can measure how up-to-date data is. Currency is a specific case of accuracy in data in the sense that out-of-date data is (usually) valid but wrong. In other words, our definition of accuracy can include currency.


## **More Information**

Here are some of the sources that illustrate the dimensions that define data quality.

- Here is a chapter from the book Data Strategy, about the four categories of data quality rules: [**How to Improve Data Quality**](http://www.informit.com/articles/article.aspx?p=399325&seqNum=3)
- This TechTarget blog post provides information on the definition of data quality as it relates. todat management and why it is important: [**Data Quality**](https://classroom.udacity.com/nanodegrees/nd002-alg-t2/parts/cd0015/modules/d9096168-9307-4d7f-8731-f07fa3cfbca4/lessons/ls2230/concepts/bd1b6c80-586b-4e5a-bbfd-1fb9decd7a38)
- Learn more about how to measure the quality of data in this YouTube video on [**The Seven Dimensions of Data Quality**](https://www.youtube.com/watch?v=dPsx8_Fcr-U), by Anish Raivadera.
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


