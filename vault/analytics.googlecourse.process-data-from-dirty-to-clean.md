---
id: hzz8zbo5j4l0uxsfowtq3il
title: Process Data from Dirty to Clean
desc: ''
updated: 1649643234090
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
**Alignment to business objective + newly discovered variables + constraints = accurate conclusions **
```

