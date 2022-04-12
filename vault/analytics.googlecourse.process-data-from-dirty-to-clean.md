---
id: hzz8zbo5j4l0uxsfowtq3il
title: Process Data from Dirty to Clean
desc: ''
updated: 1649730427234
created: 1649638993702
---
> A strong analysis depends on the integrity of the data.

### Data Integrity

The accuracy, completeness, consistency, and trustworthiness of data throughout its lifecycle.

### Data replication

The process of storing data in multiple locations.

If we are replicating data at different times in different places, there is a chance data will be out of sync. This data lacks integrity because different people might not be using same data for their findings.

### Data transfer

The process of copying data from a storage device to memory, or from one computer to another.

If the data transfer faced interruption there might be problem with data used for the analysis.

### Data manipulation

The process of changing data to make it more organized and easier to read.

Unwanted manipulation can break the data integrity.

### Other threats to the data integrity

- Human error
- Viruses(Computer Virus)
- Malware
- Hacking
- System failure


### Data constraints

| Data constraint                     | Definition                                                                                       | Examples                                                                                                                                                                                                                                                     |
| ----------------------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Data type                           | Values must be of a certain type: date, number, percentage, Boolean, etc.                        | If the data type is a date, a single number like 30 would fail the constraint and be invalid                                                                                                                                                                 |
| Data range                          | Values must fall between predefined maximum and minimum values                                   | If the data range is 10-20, a value of 30 would fail the constraint and be invalid                                                                                                                                                                           |
| Mandatory                           | Values can’t be left blank or empty                                                              | If age is mandatory, that value must be filled in                                                                                                                                                                                                            |
| Unique                              | Values can’t have a duplicate                                                                    | Two people can’t have the same mobile phone number within the same service area                                                                                                                                                                              |
| Regular expression (regex) patterns | Values must match a prescribed pattern                                                           | A phone number must match ###-###-#### (no other characters allowed)                                                                                                                                                                                         |
| Cross-field validation              | Certain conditions for multiple fields must be satisfied                                         | Values are percentages and values from multiple fields must add up to 100%                                                                                                                                                                                   |
| Primary-key                         | (Databases only) value must be unique per column                                                 | A database table can’t have two rows with the same primary key value. A primary key is an identifier in a database that references a column in which each value is unique. More information about primary and foreign keys is provided later in the program. |
| Set-membership                      | (Databases only) values for a column must come from a set of discrete values                     | Value for a column must be set to Yes, No, or Not Applicable                                                                                                                                                                                                 |
| Foreign-key                         | (Databases only) values for a column must be unique values coming from a column in another table | In a U.S. taxpayer database, the State column must be a valid state or territory with the set of acceptable values defined in a separate States table                                                                                                        |
| Accuracy                            | The degree to which the data conforms to the actual entity being measured or described           | If values for zip codes are validated by street location, the accuracy of the data goes up.                                                                                                                                                                  |
| Completeness                        | The degree to which the data contains all desired components or measures                         | If data for personal profiles required hair and eye color, and both are collected, the data is complete.                                                                                                                                                     |
| Consistency                         | The degree to which the data is repeatable from different points of entry or collection          | If a customer has the same address in the sales and repair databases, the data is consistent.                                                                                                                                                                |

> It's important check that the data you use aligns with the business objective.

### Well-aligned objectives and data

You can gain powerful insights and make accurate conclusions when data is well-aligned to business objectives. As a data analyst, alignment is something you will need to judge. Good alignment means that the data is relevant and can help you solve a business problem or determine a course of action to achieve a given business objective.

```code
Alignment to business objective + newly discovered variables + constraints = accurate conclusions
```

### Dealing with insufficient data

Types of insufficient data

- Data from only one source
- Data that keeps updating
- Outdated data
- Geographically limited data

Ways to address insufficient data

- Identify the trends with the available data
- Wait for more data if time allows
- Talk with stakeholders and adjust your objective
- Look for a new dataset

### What to do when you find an issue with your data

#### Data issue 1: no data

| Possible Solutions                                                                                                                                               | Examples of solutions in real life                                                                                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Gather the data on a small scale to perform a preliminary analysis and then request additional time to complete the analysis after you have collected more data. | If you are surveying employees about what they think about a new performance and bonus plan, use a sample for a preliminary analysis. Then, ask for another 3 weeks to collect the data from all employees. |
| If there isn’t time to collect data, perform the analysis using proxy data from other datasets.  _This is the most common workaround._                           | If you are analyzing peak travel times for commuters but don’t have the data for a particular city, use the data from another city with a similar size and demographic.                                     |

#### Data issue 2: too little data

| Possible Solutions                                            | Examples of solutions in real life                                                                                                                                                |
| ------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Do the analysis using proxy data along with actual data.      | If you are analyzing trends for owners of golden retrievers, make your dataset larger by including the data from owners of Labradors.                                             |
| Adjust your analysis to align with the data you already have. | If you are missing data for 18- to 24-year-olds, do the analysis but note the following limitation in your report: _this conclusion applies to adults 25 years and older_ _only_. |

#### Data issue 3: wrong data, including data with errors*

| Possible Solutions                                                                                                                                                                                   | Examples of solutions in real life                                                                                                                                                                |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| If you have the wrong data because requirements were misunderstood, communicate the requirements again.                                                                                              | If you need the data for female voters and received the data for male voters, restate your needs.                                                                                                 |
| Identify errors in the data and, if possible, correct them at the source by looking for a pattern in the errors.                                                                                     | If your data is in a spreadsheet and there is a conditional statement or boolean causing calculations to be wrong, change the conditional statement instead of just fixing the calculated values. |
| If you can’t correct data errors yourself, you can ignore the wrong data and go ahead with the analysis of your sample size is still large enough and ignoring the data won’t cause systematic bias. | If your dataset was translated from a different language and some translations don’t make sense, ignore the data with bad translation and go ahead with the analysis of the other data.    |

![Data Errors](/assets/images/2022-04-12-06-41-49.png)

### The importance of sample size

**Population:** All possible data values in certain dataset

**Sample size:** A part of population that is representative of the population

**Downside of the sample size:** When the population itself small, then the sample form that population might be less effective. This might lead to Sampling bias.

**Sampling bias** A sample isn't representative of the population as a whole.

Using random sampling can reduce some issues with the sampling bias.

**Random sampling:** A way of selecting a sample from a population so that every possible type of the sample has an equal chance of being chosen.

| Terminology              | Definitions                                                                                                                                                                                                                                                                                                                                                                          |
| ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Population               | The entire group that you are interested in for your study. For example, if you are surveying people in your company, the population would be all the employees in your company.                                                                                                                                                                                                     |
| Sample                   | A subset of your population. Just like a food sample, it is called a sample because it is only a taste. So if your company is too large to survey every individual, you can survey a representative sample of your population.                                                                                                                                                       |
| Margin of error          | Since a sample is used to represent a population, the sample’s results are expected to differ from what the result would have been if you had surveyed the entire population. This difference is called the margin of error. The smaller the margin of error, the closer the results of the sample are to what the result would have been if you had surveyed the entire population. |
| Confidence level         | How confident you are in the survey results. For example, a 95% confidence level means that if you were to run the same survey 100 times, you would get similar results 95 of those 100 times. Confidence level is targeted before you start your study because it will affect how big your margin of error is at the end of your study.                                             |
| Confidence interval      | The range of possible values that the population’s result would be at the confidence level of the study. This range is the sample result +/- the margin of error.                                                                                                                                                                                                                    |
| Statistical significance | The determination of whether your result could be due to random chance or not. The greater the significance, the less due to chance.                                                                                                                                                                                                                                                 |

When figuring out a sample size, here are things to keep in mind:

- Don’t use a sample size less than 30. It has been statistically proven that 30 is the smallest sample size where an average result of a sample starts to represent the average result of a population.
- The confidence level most commonly used is 95%, but 90% can work in some cases.

Increase the sample size to meet specific needs of your project:

- For a higher confidence level, use a larger sample size
- To decrease the margin of error, use a larger sample size
- For greater statistical significance, use a larger sample size

### Using statistical power

**Statistical power:** The probability of getting meaningful results from a hypothesis test

**Hypothesis testing:** A way to see if a survey or experiment has meaningful results

If a test is statistically significant, it means the results of the test are real and not an error caused by the random chance.

Usually, you need a statistical power if at least 0.8 or 80% to consider your results statistically significant.

CSV, J​SON, SQLite, and BigQuery datasets

- [credit-card-customers](https://www.kaggle.com/sakshigoyal7/credit-card-customers)
- [You-tube-trends](https://www.kaggle.com/datasnaek/youtube-new)
- [us-wildfires](https://www.kaggle.com/rtatman/188-million-us-wildfires)
- [google-analytics-sample<](https://www.kaggle.com/bigquery/google-analytics-sample)
