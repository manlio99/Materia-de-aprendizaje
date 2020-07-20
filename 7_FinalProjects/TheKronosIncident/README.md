#  The Kronos Incident

## Background
In January, 2014, the leaders of GAStech are celebrating their new-found fortune as
a result of the initial public offering of their very successful company. In the midst of this celebration, several
employees of GAStech go missing. An organization known as the Protectors of Kronos (POK) is suspected in
the disappearance, but things may not be what they seem.


## Task 1: The Kidnapping and a Historical Analysis of the Protectors of Kronos

Your task is to bring law enforcement up to date on the current organization of the POK and how that organization has changed over time, as well as to characterize the events surrounding the disappearance. You are provided with a set of current and historical news reports at your disposal, as well as resumes of numerous GAStech employees and email headers from two weeks of internal GAStech company email. You are being
counted on to bring law enforcement up to date on the current organization of the POK and how that organization has changed over time, as well as to characterize the events surrounding the disappearance.

### Data - *[Download](https://github.com/emmanueliarussi/DataScienceCapstone/tree/master/7_FinalProjects/TheKronosIncident/data/task1.zip)*

The data provided consists of a collection of text-based files dealing with the kidnapping of the GASTech employees by members of the social movement group POK.  As an analyst, you have the following data at your disposal:

* A map of Kronos
* A chart describing the local GAStech organization, in PDF format.
* A spreadsheet of GAStech employee records, in Microsoft Excel format. The primary worksheet contains the data; the index worksheet contains the data dictionary
* Email headers from two weeks of internal GAStech company email, in comma-separated values (CSV) format
* Resumes and short biographies of many, but not all, of the GAStech employees, in Microsoft Word format
* Historical reports and descriptions of the countries involved, in Microsoft Word format
* Relevant current and historical news reports from multiple domestic and translated foreign sources, in text file format. Because these articles have come from multiple sources and original formats, some of the them may contain corrupted characters, which is typical for this type of data. These corrupted characters should not interfere with your ability to analyze the data.

### Goals

1. Provide a clear analysis of the structure of the Protectors of Kronos network, with supporting evidence.
    1. Who are the leaders?
    2. Who is part of the extended network?
    3. How has the group structure and organization changed over time?
    4. Where are the potential connections between the POK and GAStech?
2. Describe the events of January 20-21, 2014. What is the timeline of events? 
3. Provide at least two possible explanations why the GAStech employees may be missing. What evidence do you have to support each of these explanations?

In order to explore this data, you will need to perform several kinds of data integration activities and analyses to generate hypotheses
about the __missing employees__. The main structure of the POK is described in the two historical reports dated five and ten years ago. Updates can be found in news articles and in some of the other datasets. Your investigation into this text data can be supported by text analytic tools. When analysing emails headers (containing *To*, *From*, *Date*, and *Subject* fields) try to reconstruct some sort of a communication network within the GASTech organization during the period for which data was provided. You should find clues to POK members or sympathizers plus hints at socialization patterns among employees. 

## Task 2: Geospatial-Temporal Patterns of Life Analysis

Many of the Abila, Kronos-based employees of GAStech have company cars which are approved for both personal and business use. Those who do not have company cars have the ability to check out company trucks for business use, but these trucks cannot be used for personal business. Employees with company cars are happy to have these vehicles, because the company cars are generally much higher quality than the cars they would be able to afford otherwise. However, GAStech does not trust their employees. Without the employees’ knowledge, GAStech has installed geospatial tracking software in the company vehicles. The vehicles are tracked periodically as long as they are moving.

This vehicle tracking data has been made available to law enforcement to support their investigation. Unfortunately, data is not available for the day the GAStech employees went missing. Data is only available for the two weeks prior to the disappearance. In addition to the vehicle data, law enforcement has been given access to the personal and business credit and debit card transactions for the local GAStech employees for the two weeks preceding the kidnapping. Many of the GAStech employees also use loyalty cards to gain discounts or extra benefits at the businesses they patronize, and law enforcement has been given access to two weeks of this loyalty card data as well.

As a data scientist expert assisting law enforcement, your mission is to make sense of this data to identify suspicious patterns of behavior and to prioritize which of these may be related to the missing staff members. You must cope with uncertainties that result from missing, conflicting, and imperfect data to make recommendations for further investigation.


### Data - *[Download](https://github.com/emmanueliarussi/DataScienceCapstone/tree/master/7_FinalProjects/TheKronosIncident/data/task2.zip)*
As an analyst, you have the following data at your disposal:

1. A list of vehicle assignments by employee, in CSV format (`car-assignments.csv`)
    1. Employee Last Name
    2. Employee First Name
    3. Car ID (integer)
    4. Current Employment Type (Department; categorical)
    5. Current Employment Title (job title; categorical)
2. ESRI shapefiles of Abila and Kronos (in the Geospatial folder)
    1. A CSV file of vehicle tracking data (`gps.csv`)
    2. Timestamp
    3. Car ID (integer)
    4. Latitude
    5. Longitude
3. A CSV file containing loyalty card transaction data (`loyalty_data.csv`)
    1. Timestamp
    2. Location (name of the business)
    3. Price (real)
    4. FirstName (first name of the card holder)
    5. LastName (last name of the card holder)
4. A CSV file containing credit and debit card transaction data (`cc_data.csv`)
    1. Timestamp
    2. Location (name of the business)
    3. Price (real)
    4. FirstName (first name of the card holder)
    5. LastName (last name of the card holder)
A tourist map of Abila with locations of interest identified, in JPEG format (`map-tourist.jpg`)

### Goals

1.  Describe common daily routines for GAStech employees. What does a day in the life of a typical GAStech employee look like? 

2. Identify up to twelve unusual events or patterns that you see in the data. If you identify more than twelve patterns during your analysis, focus your answer on the patterns you consider to be most important for further investigation to help find the missing staff members. For each pattern or event you identify, describe
    1. What is the pattern or event you observe?
    2. Who is involved?
    3. What locations are involved?
    4. When does the pattern or event take place?
    5. Why is this pattern or event significant?
    6. What is your level of confidence about this pattern or event? Why?

3. Like most datasets, the data you were provided is imperfect, with possible issues such as missing data, conflicting data, data of varying resolutions, outliers, or other kinds of confusing data. Considering data is primarily spatiotemporal, describe how you identified and addressed the uncertainties and conflicts inherent in this data to reach your conclusions in questions 1 and 2.

In order to use this data, you will require skills in geospatial-temporal analysis, along with the ability to combine various types of data in sensible ways. The GPS data was extracted from the cars for the two weeks period prior to the kidnapping, but not including the kidnapping day itself.  GASTech also issued company debit/credit cards that could be used for personal spending, and many employees had loyalty cards for restaurants and shops around Abila city. Analyzing the combined data sources could reveal clues about the kidnapping and the GASTech employees who may have participated in this activity.  You need to be aware that some GPS readings may be skewed for some vehicles. In addition, particular locations may exhibit deviations in the times at which they post their card transactions. Similarly, in some cases, the transactions were logged in batches once per day; in some locations transactions may be delayed, creating the appearance of individuals shopping in the middle of the night. 

Focus your work on identifying regular patterns. For example, credit card data may contain typical charges like GASTech employees preferring to use their debit and loyalty cards at coffee houses. Deviations from these patterns might indicate suspicious activities or just non-conforming patterns by individuals. Hypotheses about suspicious activities need to be supported by evidence and/or reasoning from data. Look for anomalies such as a credit card charge occurring for an employee while the GPS track indicates a different location for their assigned vehicle. 

Map data, including shape files of Abila city streets and a visitor’s map of the city sites and shops, are provided to you as an additional support to understand patterns of life. For example, even though employees’ home addresses were not provided, patterns of life analysis may reveal where they spent their evening hours, typically indicating their home address. Regular gatherings at what appeared to be residences, but not corresponding to any employee’s home address could suggest different hypotheses.

## Deliverables

Please prepare __a single python notebook__ with the answers __for each task__. However, feel free to use more than a single python file to solve tasks. If necessary, some results may be pre-computed and stored in separate files. Notebooks must clearly explain the answers to each question, supported by evidence derived from the data and visualized using the tools seen in the course. Describe the characteristics of the data you were given as well as your reasoning process leading to each answer. Use the following structure template for the answers notebook:

- project title, task name
    - description and data characterization 
    - answer question 1
    - answer question 2
    - ...
