# Querying Data Warehouse using PostgreSQL
Populate and query Data Warehouse using PostgreSQL - PgAdmin

## Objectives:
Apply CUBE and ROLLUP functions to speed the retrieval of aggregated data using materialized views. And you can identify when an organization benefits by using staging areas for data storage and retrieval.<br>

This project is from **"Getting Started with Data Warehousing and BI Analytics"** course offerred by **IBM** in **Coursera**. 


## Database: 
The database used in this lab. contains the following tables:
  * DimCustomer
  * DimMonth
  * FactBilling<br>
  
A cloud service provider has provided us with their billing data. This file contains billing data from the past 10 years. We need to design a data warehouse to support insightful queries on this data.<br>

* **DimCustomer** <br><br>
![DimCustomer](/Snapshots/DimCustomer.png) <br><br>

* **DimMonth** <br><br>
![DimMonth](/Snapshots/DimMonth.png) <br><br>

* **FactBilling** <br><br>
![FactBilling](/Snapshots/FactBilling.png) <br><br>

* **Schema** <br><br>
![StarSchema](/Snapshots/StarSchema.png) <br><br>


## Grouping sets Query
To create a grouping set for three columns labeled year, category, and sum of billedamount.<br>
The output will contain 13 rows. The code and the partial output can be seen in the image below.<br><br>
![grouping sets](/Snapshots/GroupingSet.png) <br><br>


## Rollup Query
To create a rollup using the three columns year, category and sum of billedamount.<br>
The output will contain 408 rows. The code and the partial output can be seen in the image below.<br><br>
![Rollup](/Snapshots/Rollup.png) <br><br>


## Cube Query
To create a cube using the three columns labeled year, category, and sum of billedamount.<br>
The output will contain 468 rows. The code and the partial output can be seen in the image below.<br><br>
![Rollup](/Snapshots/Rollup.png) <br><br>


## Create a Materialized Query Table(MQT)
The following command creates an MQT named countrystats that has 3 columns.
- country
- year
- totalbilledamount<br>

![MQT](/Snapshots/MQT.png) <br><br>

MQT is essentially the result of the below query, which gives you the country, year and the sum of billed amount grouped by country and year.<br>

![MQT](/Snapshots/MQTresult.png) <br><br>

