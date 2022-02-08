# DataWarehousing_TechnicalPaper
Data Warehousing

# DATA WAREHOUSING

In this section, we will discuss about Data warehousing, architecture and different approaches

<br>

<span style="font-size:20px">

### Contents

<span style="font-size:167x">

- <a href='#dw'>What is Data Warehousing ?</a>

- <a href='#char'>Characteristics</a>

- <a href='#arch'>Architecture</a>

- <a href='#stages'>Stages of Data Warehousing</a>

- <a href='#approaches'>Different Approaches</a>

- <a href='#adv'>Advantages and Disadvantages</a>
  
- <a href='#References'>References</a>

<br>

<h2 id='dw'>1. What is Data Warehousing ?</h2>

A **Data Warehouse** is a central repository of integrated data used for reporting and data analysis. It is also known as Enterprise Data Warehouse, stores current and historical data at one place.
<br>

Data warehousing is the process of constructing and using a data warehouse.It involves data cleaning, data integration, and data consolidations.
<br>

A data warehouse can contain multiple databases. In each database, data is organized into tables and columns. Tables can be organized inside the schemas. In each column, description of the data can be given. When data is ingested, it is stored in various tables described by the schema.

<br>

<h2 id='char'>2. Characteristics</h2>

Below are the major characteristics of data warehouse:
<br>

![](https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-9-1.png)

- **Subject-oriented**

    A data warehouse can be used to analyze a particular subject area. Gathering the required objects is called subject-oriented, this is useful in decision making.

- **Integrated**

    A data warehouse integrates data from multiple resources. Since it comes from various operational systems, all inconsistencies must be removed. Consistencies such as naming conventions, measurement of variables, encoding structures, physical attributes of data and so on.

- **Time-variant**

    Data warehouse stores the historical data. It is mainly meant for data mining and forecasting.<br>
    For example : One can retrieve data from 6 months, 12 months, or even older data from a data warehouse.

- **Non-volatile**

    The data in the data warehouse is read-only, which means it cannot be updated, created, or deleted.

<br>
<h2 id='arch'>3. Architecture</h2>

Three-Tier Data Warehouse Architecture

Following are the three tiers of the data warehouse architecture :

**Bottom Tier** − The bottom tier of the architecture is the data warehouse database server. It is the relational database system. We use the back end tools and utilities to feed data into the bottom tier. These back end tools and utilities perform the Extract, Clean, Load, and Refresh functions.

**Middle Tier** − In the middle tier, we have the OLAP Server that can be implemented in either of the following ways.

- Relational OLAP (ROLAP), which is an extended RDBMS. The ROLAP maps the operations on multidimensional data to standard relational operations.

- Multidimensional OLAP (MOLAP) model, which directly implements the multidimensional data and operations.

**Top-Tier** − This tier is the front-end client layer. This layer holds the query tools and reporting tools, analysis tools and data mining tools.

The following picture shows the three-tier architecture of data warehouse:

![](https://www.tutorialspoint.com/dwh/images/dwh_architecture.jpg)

<br>
<h2 id='stages'>4. Stages of Data Warehousing</h2>
There are at least seven stages to the creation of a data warehouse, they include:

  1. Determining the business objectives and its key performance indicators.
1. Collecting and analyzing the appropriate information.
2. Identifying the core business processes that contribute the key data.
3. Constructing a conceptual data model that shows how the data are displayed to the end-user.
4. Locating the sources of the data and establishing a process for feeding data into the warehouse.
5. Establish a tracking duration. Data warehouses can become unwieldy. Many are built with levels of archiving, so that older information is retained in less detail.
6. Implementing the plan.

<br>

<h2 id='approaches'>5. Different Approaches</h2>

Extract, transform, load (ETL) and extract, load, transform (ELT) are the two main approaches used to build a data warehouse system. 


- **ETL-based data warehousing**

    The extract, transform, load (ETL)-based data warehouse uses staging, data integration, and access layers to house its key functions. The staging layer stores raw data extracted from each of the heterogeneous source data systems. The integration layer integrates the different data sets by transforming the data from the staging layer by storing this transformed data in an operational data store (ODS) database. The integrated data are then moved to another database called data warehouse database. The access layer helps users retrieve data.

    ![](https://static.javatpoint.com/tutorial/datawarehouse/images/difference-between-etl-and-elt.png)



- **ELT-based data warehousing**

    ELT-based data warehousing don't have a separate ETL tool for data transformation. Instead, it maintains a staging area inside the data warehouse itself. In this approach, data gets extracted from different source systems and are then directly loaded into the data warehouse, before any transformation occurs. All necessary transformations are then handled inside the data warehouse itself. Finally, the modified data gets loaded into target tables in the same data warehouse. 

    ![](https://static.javatpoint.com/tutorial/datawarehouse/images/difference-between-etl-and-elt-1.png)

<br>
<h2 id='adv'>6. Advantages and Disadvantages</h2>

**Advantages**
<br>
Complete control over the four main areas of data management systems: 
 - Clean data
 - Query processing: multiple options 
 - Indexes: multiple types 
 - Security: data and access

**Disadvantages** 
- Adding new data sources takes time and associated high cost. 
- Data owners lose control over their data, raising ownership, security and privacy issues. 
- Long initial implementation time and associated high cost. 
- Difficult to accommodate changes in data types and ranges, data source schema, indexes and queries. 

<h2 id='ref'>7. References</h2>

>https://www.javatpoint.com/data-warehouse-etl-vs-elt
 
>https://www.geeksforgeeks.org/characteristics-and-functions-of-data-warehouse/
   
>https://www.itprotoday.com/sql-server/7-steps-data-warehousing
