# Let's Assess our Data 👨‍💻 
The Data Wrangling process consists of three steps:

- Gathering 🎣
- Assessing [**🧐**](https://emojipedia.org/face-with-monocle/)
- Cleaning 🧼

Cleaning comes after assessment. Cleaning something you aren't aware of is impossible! Here, I'll be sharing what I've learned about seeing and classifying typical problems with data quality and organization.

The second phase in the data wrangling process is assessing your data. When assessing, you look at two aspects of your data set:

Issues with data quality including content problems, such as missing, duplicate, or erroneous data. We refer to this as unclean data.

Lack of tidiness : Data with unique structural problems that make it more difficult to clean, analyze, visualize, or model your data afterwards.


## Unclean Data: Messy versus Dirty

Unclean data can be of two different types:


- Low quality data, commonly referred to as **dirty data. Content problems** exist with low-quality data.
- Untidy data is another name for **messy data**. Data that is messy has **structural concerns.**

Clean data are those in which each variable is represented by a column, each observation by a row, and each category of observational unit by a table. Hadley Wickham, the creator of the tidy data format, refers to any other arrangement as messy in his tidy data paper.


## Types of Assessment

There are two ways to evaluate your data: **visually** and **programmatically**. 

**Visual evaluation** is simply opening the data in pandas, a text editor, or a spreadsheet program, for example, and viewing it all at once.

As the name implies, **programmatic assessment** employs code to view particular portions of the data, such as using functions or methods to summarize the data. 
Like the .info technique, as an illustration. Even though you can plot the data, wrangling rarely involves graphing.


## Steps Of Assessing Data

The process of assessing data can be divided into two parts, regardless of the form of evaluation you're employing;


- Identifying a problem in your data
- Documenting that problem

This method works whether you analyze your data programmatically or visually. You don't have to describe a fix when documenting a problem, as that comes under the cleaning step of data wrangling.


## Documentation

Why not simply describe what has to be done to resolve the problems instead of first documenting any dirty issues we notice? 
Writing detailed instructions for each problem in your data can become difficult, time-consuming, and confusing as it becomes more complex. Trying to figure out how to clean something intricate right away after capturing it can get overwhelming.

Writing simply observations as a first stage is important practice if you are separating the assessing and cleaning steps of data wrangling.
You can skip the observation and jump right into specifying how to clean it if you decide to identify a problem then fix it right away (which is totally acceptable). This is the *Define-Code-Test* cleaning framework


## Step by Step Journey

Here I will be doing my Practice for both the the Visual Data Assessment and Programmatic Assessment.




