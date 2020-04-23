# Introduction #

This is blog as part of my in Udacity DataScience nanao degree. This blogpost documents the process and outcome of applying the CRISP-DM 
process to answer bsuiness questions. 

The data set used is the **Stack Overflow Data - 2017 Survey** that was provided with the course material. I came up with four business 
question I wanted to answer from the dataset. These questions are:

### Questions of Interest ###

- Q1. What are the most popular languages by country
- Q2. Is there a correlation between most popular languages choice and job satisfaction
- Q3. How does parent's highest education relate to highest respondent education
- Q4. Does remote work increase need for StackoverFlow? 

## Get the data, check the data, and clear the way

The first step is getting the data. But before we do that - it is relevant to state the tools we will be using for the data analysis. 
I worked with Python in a Jupyter Notebook and Pandas & Matplotlib. 

The data was already provided in a cvs format; this make the data acollection step, not required. The files were moved to the relevant 
folders Pandas read_csv was used to import the data. 

Below is a snapshop of the dataframe head.


![The Data](TheData.JPG)


The data was clean and not much pre-processing was required. Additional processing was done to answer each quesion, and we will see that later in the blog.


Below is a description of the data:

![Data Description](Data2.JPG)



The data package also includes a schema that provides the survey questions. See a snapshot below.

![The Data Schema](Schema1.JPG)


#Question 1 - What are the most popular languages by country
To answer the first question I used the **Country** and **HaveWorkedLanguage** columns. The **Country** column was straing forward and provided a single entry - the country of the respondent - but **HaveWorkedLanguage** column needed additional processing. Each entry was 
a concatenated string of all the languages the responded has worked with, separated by a semi-colon. The unique value of each language was needed to find our their popularity by country.

As this processing was anticipated to be likley useable in other cases, a dedicated functon was defined to do the processing. 


