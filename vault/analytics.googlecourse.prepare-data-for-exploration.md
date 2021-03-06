---
id: xesrjl7c0rhhtag0jjdbyvi
title: Prepare Data for Exploration
desc: ''
updated: 1649382080766
created: 1648258928874
---

## How data is collected

Below are the commonly used data collected methods.

- Interview
- Observations
- Forms
- Questionnaires
- Surveys
- Cookies

## Data collection considerations

- How the data will be collected
- Choose data sources
- Decide what data to use
- How much data to collect
- Select the right data type
- Determine the time frame

### First-party data(Preferred method)

Data collected by an individual or group using their own resource.

### Second-party data

Data collected by a group directly from its audience and then sold.

### Third-party data

Data collected from outside sources who did not collect it directly.

Decide if you will collect the data using your own resources or receive (and possibly purchase it) from another party. Data that you collect yourself is called **First-party data**.

If you don’t collect the data using your own resources, you might get data from second-party or third-party data providers. **Second-party data** is collected directly by another group and then sold. **Third-party data** is sold by a provider that didn’t collect the data themselves. Third-party data might come from a number of different sources.

#### Population

All possible data values in a certain dataset.

#### Sample

A part of population that is representative of the population.

![Data collection considerations chart](/assets/images/2022-03-27-09-22-51.png)

## Discover data formats

### Discrete data

Data that is counted and has a limited number of values.

### Continuous data

Data that is measured and can have almost any numeric value.

### Nominal data

A type of qualitative data that is categorized without a set order.

### Ordinal data

A type of qualitative data with a set order or scale.

### Internal data

Data that lives within a company's own systems.

### External data

Data that lives and is generated outside an organization.

### Structure data

Data organized in a certain format such as rows and columns.

### Unstructured data

Data that is not organized in any easily identifiable manner.

## Formats of data in practice

Choosing the right format will help you manage and use your data in the best way possible.

![Data formats](/assets/images/2022-03-27-09-06-46.png)

### Primary vs. Secondary

Data Format Classification | Definition | Examples
---------|----------|---------
 Primary data | Collected by a researcher from first-hand sources | Data from an interview you conducted, Data from a survey returned from 20 participants, Data from questionnaires you got back from a group of workers
 Secondary data | Gathered by other people or from other research | Data you bought from a local data analytics firm’s customer profiles, Demographic data collected by a university, Census data gathered by the federal government

### Internal vs. External

Data Format Classification | Definition | Examples
---------|----------|---------
 Internal data | Data that lives inside a company’s own systems | Wages of employees across different business units tracked by HR, Sales data by store location, Product inventory levels across distribution centers
 External data | Data that lives outside a company or organization | National average wages for the various positions throughout your organization, Credit reports for customers of an auto dealership

### Continuous vs. Discrete

Data Format Classification | Data Format Classification | Examples
---------|----------|---------
 Continuous data | Data that is measured and can have almost any numeric value | Height of kids in third grade classes (52.5 inches, 65.7 inches), Runtime markers in a video, Temperature
 Discrete data | Data that is counted and has a limited number of values | Number of people who visit a hospital on a daily basis (10, 20, 200), Room’s maximum capacity allowed, Tickets sold in the current month

### Qualitative vs. Quantitative

Data Format Classification | Definition | Examples
---------|----------|---------
 Qualitative | Subjective and explanatory measures of qualities and characteristics | Exercise activity most enjoyed, Favorite brands of most loyal customers, Fashion preferences of young adults
 Quantitative | Specific and objective measures of numerical facts | Percentage of board certified doctors who are women, Population of elephants in Africa, Distance from Earth to Mars

### Nominal vs. Ordinal

Data Format Classification | Definition | Examples
---------|----------|---------
 Nominal | A type of qualitative data that isn’t categorized with a set order | First time customer, returning customer, regular customer, New job applicant, existing applicant, internal applicant, New listing, reduced price listing, foreclosure
 Ordinal |  A type of qualitative data with a set order or scale | Movie ratings (number of stars: 1 star, 2 stars, 3 stars), Ranked-choice voting selections (1st, 2nd, 3rd), Income level (low income, middle income, high income)

### Structured vs. Unstructured

Data Format Classification | Definition | Examples
---------|----------|---------
 Structured data | Data organized in a certain format, like rows and columns | Expense reports, Tax returns, Store inventory
 Unstructured data | Data that isn’t organized in any easily identifiable manner | Social media posts, Emails, Videos

### Data model

A model that is used for organizing data elements and how they relate one another.

### Data elements

Pieces of information, such as people's names, account numbers, and addresses.

## Data modeling levels and techniques

### What is data modeling?

Data modeling is the process of creating diagrams that visually represent how data is organized and structured.  These visual representations are called data models. You can think of data modeling as a blueprint of a house. At any point, there might be electricians, carpenters, and plumbers using that blueprint. Each one of these builders has a different relationship to the blueprint, but they all need it to understand the overall structure of the house. Data models are similar; different users might have different data needs, but the data model gives them an understanding of the structure as a whole.

### Levels of data modeling

![Levels of data modeling](/assets/images/2022-03-28-07-22-05.png)

1. **Conceptual data modeling** gives a high-level view of the data structure, such as how data interacts across an organization. For example, a conceptual data model may be used to define the business requirements for a new database. A conceptual data model doesn't contain technical details.
2. **Logical data modeling** focuses on the technical details of a database such as relationships, attributes, and entities. For example, a logical data model defines how individual records are uniquely identified in a database. But it doesn't spell out actual names of database tables. That's the job of a physical data model.
3. **Physical data modeling** depicts how a database operates. A physical data model defines all entities and attributes used; for example, it includes table names, column names, and data types for the database.

[Data Modeling - Conceptual, Logical, and Physical Data Models](https://www.1keydata.com/datawarehousing/data-modeling-levels.html)

[3 Basic Data Modeling Techniques - ERD, UML and Data Dictionary - Dataedo Blog](https://dataedo.com/blog/basic-data-modeling-techniques)

## Data types fields, and values

### Data type

A specific kind of data attribute that tells what kind of value the data is.

### Data types in spreadsheets

- Number
- Text or string
- Boolean

### Wide data

Data in which every data subject has single row with multiple columns to hold the values of various attributes of the subject.

### Long data

Data in which each row is one time point per subject, so each subject will have data in multiple rows.

## Transforming data

### What is data transformation?

**Data transformation** is the process of changing the data’s format, structure, or values.

Data transformation usually involves:

- Adding, copying, or replicating data
- Deleting fields or records
- Standardizing the names of variables
- Renaming, moving, or combining columns in a database
- Joining one set of data with another
- Saving a file in a different format. For example, saving a spreadsheet as a comma separated values (CSV) file.

Wide data is preferred when | Long data is preferred when
---------|----------
 Creating tables and charts with a few variables about each subject | Storing a lot of variables about each subject. For example, 60 years worth of interest rates for each bank
 Comparing straightforward line graphs | Performing advanced statistical analysis or graphing

### Bias

A preference in favor of or against a person, group of people, or thing.

### Data bias

A type of error that systematically skews results in a certain direction.

### Sampling bias

When a sample isn't representative of the population as a whole.

### Unbiased sampling

When a sample is representative of the population being measured.

### Observer bias (experimenter bias / research bias)

The tendency for different people to observe things differently.

### Interpretation bias

The tendency to always interpret ambiguous situations in a positive or negative way.

### Confirmation bias

The tendency to search for or interpret information in a way that confirms pre-existing beliefs.

### Identifying good data sources

- **R**eliable
- **O**riginal
- **C**omprehensive
- **C**urrent
- **C**ited

> "Every good solution is found by avoiding bad data"

## Ethics of data

### Ethics

Well-founded standards of right and wrong that prescribe what humans ought to do, usually in terms of rights, obligations, benefits to society fairness, or specific virtues.

### Data Ethics

Well-founded standards of right and wrong that dedicate how data is collected, shared, and used.

### Ownership

Individuals own the raw data they provide, and they have primary control over its usage, how it's processed, and how it's shared.

### Transaction transparency

All data-processing activities and algorithms should be completely explainable and should be completely explainable and understood by the individual who provides their data.

### Consent

An individual's right to know explicit details about how and why their data will be used before agreeing to provide it.

### Currency

Individuals should be aware of financial transactions resulting from the use of their personal data and the scale of these transactions.

### Privacy (data protection)

Preserving a data subject's information and activity any time a data transaction occurs.

- Protecting from unauthorized access to our private data
- Freedom from inappropriate use of our data
- The right to inspect, update, or correct our data
- Ability to give consent to use our data
- Legal right to access the data

### Sites and resources for open data

1. [U.S. government data site](https://www.data.gov/): Data.gov is one of the most comprehensive data sources in the US. This resource gives users the data and tools that they need to do research, and even helps them develop web and mobile applications and design data visualizations.
2. [U.S. Census Bureau](https://www.census.gov/data.html): This open data source offers demographic information from federal, state, and local governments, and commercial entities in the U.S. too.
3. [Open Data Network](https://www.opendatanetwork.com/): This data source has a really powerful search engine and advanced filters. Here, you can find data on topics like finance, public safety, infrastructure, and housing and development.
4. [Google Cloud Public Datasets](https://cloud.google.com/public-datasets): There are a selection of public datasets available through the Google Cloud Public Dataset Program that you can find already loaded into BigQuery.
5. [Dataset Search](https://datasetsearch.research.google.com/): The Dataset Search is a search engine designed specifically for data sets; you can use this to search for specific data sets.

## Databases in data analytics

### Relational database

A database that contains a series of related tables that can be connected via their relationships.

![The key to relational databases](/assets/images/2022-04-01-06-24-06.png)

### Primary key

An Identifier that references a column in which each value is unique.

- Used to ensure data in a specific column is unique
- Uniquely identifies a record in a relational database table
- Only one primary key is allowed in a table
- Cannot contain null or blank values

### Foreign key

A field within a table that is a primary key in another table.

- A column or group of columns in a relational database table that provides a link between the data in two tables
- Refers to the field in a table that's the primary key of another table
- More than one foreign key is allowed to exist in a table.

### Metadata

> "Metadata is data about the data".

Metadata is used in database management to help data analysts interpret the contents of the data within the database.

### There common types of metadata

- Descriptive
- Structural
- Administrative

#### Descriptive

Metadata that describes a piece of data and can be used to identify it at a later point in time.

#### Structural

Metadata that indicates how a piece of data is organized and whether it is part of one, or more than one, data collection.

#### Administrative

Metadata that indicates the technical source of a digital asset.

### Elements of metadata

**Title and description:** What is the name of the file or website you are examining? What type of content does it contain?

**Tags and categories:** What is the general overview of the data that you have? Is the data indexed or described in a specific way?

**Who created it and when:** Where did the data come from, and when was it created? Is it recent, or has it existed for a long time?

**Who last modified it and when:** Were any changes made to the data?  If yes, were the modifications recent?

**Who can access or update it:** Is this dataset public? Are special permissions needed to customize or modify the dataset?

### Metadata repository

A database specifically created to store metadata.

**Metadata repositories:** make it easier and faster to bring together multiple source for data analysis.

- Describe the state and location of the metadata
- Describe the structure of the table inside
- Describe how the data flows through the repository
- Keep track of who accesses the metadata and when

### Data governance

A process to ensure the formal management of a company's data assets.

### Exploring public datasets

- [Datasets Google Cloud](https://cloud.google.com/public-datasets)
- [Dataset Search](https://datasetsearch.research.google.com/)
- [Kaggle](https://www.kaggle.com/datasets?utm_medium=paid&utm_source=google.com+search&utm_campaign=datasets&gclid=CjwKCAiAt9z-BRBCEiwA_bWv-L6PpACh6RzmrJjQjmNGCCE7kky1FCtc6Jf1qld-4NwDMYL0WsUyxBoCdwAQAvD_BwE)
- [BigQuery public datasets | Google Cloud](https://cloud.google.com/bigquery/public-data)

#### Public health datasets

- [Data collections - WHO](https://www.who.int/data/collections)
- [The Cancer Imaging Archive (TCIA) datasets | Cloud Healthcare API | Google Cloud](https://cloud.google.com/healthcare/docs/resources/public-datasets/tcia)
- [1000 Genomes | Cloud Life Sciences Documentation | Google Cloud](https://cloud.google.com/life-sciences/docs/resources/public-datasets/1000-genomes)

#### Public climate datasets

- [National climatic data center](https://www.ncdc.noaa.gov/data-access/quick-links)
- [Dataset Gallery | NOAA Climate.gov](https://www.climate.gov/maps-data/datasets)

#### Public social-political datasets

- [The State of the World's Children 2019 Statistical Tables - UNICEF DATA](https://data.unicef.org/resources/dataset/sowc-2019-statistical-tables/)
- [CPS Tables](https://www.bls.gov/cps/tables.htm)
- [The Stanford Open Policing Project](https://openpolicing.stanford.edu/)

### Best practices when organizing data

- Work out and agree on file naming conventions early on in a project to avoid renaming files again and again.
- Align your file naming with your team's or company's existing file-naming conventions.
- Ensure that your file names are meaningful; consider including information like project name and anything else that will help you quickly identify (and use) the file for the right purpose.
- Include the date and version number in file names; common formats are YYYYMMDD for dates and v## for versions (or revisions).
- Create a text file as a sample file with content that describes (breaks down) the file naming convention and a file name that applies it.
- Avoid spaces and special characters in file names. Instead, use dashes, underscores, or capital letters. Spaces and special characters can cause errors in some applications.

### Data security

Protecting data from unauthorized access or corruption by adopting safety measures.

**Encryption:** uses a unique algorithm to alter data and make it unusable by users and applications that don’t know the algorithm. This algorithm is saved as a “key” which can be used to reverse the encryption; so if you have the key, you can still use the data in its original form.

**Tokenization:** replaces the data elements you want to protect with randomly generated data referred to as a “token.” The original data is stored in a separate location and mapped to the tokens. To access the complete original data, the user or application needs to have permission to use the tokenized data and the token mapping. This means that even if the tokenized data is hacked, the original data is still safe and secure in a separate location.
