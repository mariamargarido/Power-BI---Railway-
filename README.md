# UK Railway Data Analytics Dashboard - Power BI

## Project Overview

This project was developed as a technical solution for the **UK Ministry of Tourism** to analyze train journey patterns, service performance, and the financial impact of refunds across the United Kingdom.

The primary goal was to transform raw transactional data into a scalable, automated, and decision-oriented reporting tool that allows for both strategic and operational analysis.

## Key Features

* 
**End-to-End BI Cycle:** Covers all phases: ETL, Data Modeling, DAX Measures, and Data Storytelling.


* 
**Automated Data Pipeline:** Built using "Get Data > Folder" to ensure the model updates automatically as new monthly CSV files are added.


* 
**Advanced Analytics:** Includes punctuality performance, revenue breakdown by ticket class, and root cause analysis for delays.


* 
**Dynamic Refund Logic:** Implementation of a complex refund policy based on delay duration (15 to 60+ minutes).



## Technical Architecture

### 1. ETL & Data Transformation (Power Query)

Data cleaning and standardization were performed to ensure dataset consistency:

* 
**Handling Missing Values:** Replaced 87% of missing "Reason for Delay" values with "Unknown" and standardized railcard entries.


* 
**Data Standardization:** Unified inconsistent text entries (e.g., typos like "Adul" to "Adult" and case sensitivity in delay reasons).


* 
**Custom Business Logic:** Created calculated columns for **Refund Amount**, **Refund Granted**, and **Journey Routes**.



### 2. Data Modeling

The project utilizes a **Star Schema** to optimize performance and simplify analysis:

* 
**Fact Table:** `Railway_Facts` containing transactional records and key metrics.


* 
**Dimension Tables:** Normalized tables for `Tickets`, `Railcards`, `Purchase Channels`, `Payment Methods`, and `Delays`.


* 
**Time Intelligence:** A dedicated `DatasUnicas` (Calendar Table) to support complex time-based slicers and historical comparisons.



### 3. DAX Measures

Several measures were implemented to provide dynamic insights:

* 
`Transaction_Count`: Total number of journeys.


* 
`Delay_Minutes`: Calculation of scheduled vs. actual arrival times.


* 
`Refund_Amount`: DAX logic applied to calculate financial impact based on delay tiers (25%, 50%, or 100%).


* 
`Days_Before_Journey`: Lead time analysis between purchase and travel.



## Dashboard Structure

The final report consists of 5 specialized pages designed for different stakeholders:

1. 
**Executive Summary:** High-level KPIs including total sales, total journeys, and overall delay rates.


2. 
**Routes Analysis:** Popularity ranking and geographic analysis via interactive maps.


3. 
**Ticket Analysis:** Revenue breakdown by ticket type (e.g., Advance, Off-Peak) and class.


4. 
**Customer Behavior:** Analysis of purchase channels and lead times.


5. 
**Delays & Refunds:** Deep dive into the main causes of delays and their associated compensation costs.



## Tools Used

* 
**Power BI Desktop** (Data Modeling & Visualization) 


* 
**Power Query** (M Language for ETL) 


* 
**DAX** (Data Analysis Expressions) 


