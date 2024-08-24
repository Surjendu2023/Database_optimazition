# database_optimazition

## Brifing about the project:
   As a Lead data analyst at Airtel,My main goal is to analysis the data.With the user base of 280M+ it's become nightmare to handle or store this amount of data. 
   hence, I have followed few steps to store 280 M+ user base and with some optimization technic i could able to querying my databases.

# STEP 1: First to calculate the data volume
          As checked with the previous records,data volume i receive from Various sources is approx 6L rows/day.
          and my aim is to store atleast 1 Year data and the data volume would be as below:
          per day data volume=600000 rows/day
          per year data volume=600000*365 =21,90,00,000/Year
          converting into Millions=21,90,00,000/1000000=219 Millions

 # STEP 2: Calculate the storage require to store 219 Millions user base

            Number of rows=219 million
            Number of columns = 26
            Length of each column = 255 bytes
            Total Size =21,90,00,000 rows * 26 Columns * 255 bytes/(1024^3)
            Toal Spece Require= 1834.74 GB

# STEP 3 : Identify the Platform to store the data flow
           We can store this data into any cloud services(AWS,GCP,Azure) or any Relational Databases.
           In My case,I will be using Oracle SQL Server to store the data flow

# STEP 4 : Extract,Transform,Load(ETL) into Datawarehouse          



# STEP 5 : Query Execution Plan (Avioding Full Table Scan)



# STEP 6 : Normalization on Tables

Normalization is the process of organizing data in the database to reduce redundancy and improve data integrity. 
The main goal of normalization is to split the data into smaller, more manageable tables. This makes it easier to update and maintain the data, and it also reduces the amount of duplicated data, which can lead to inconsistencies.

For example, let’s consider a database that stores information about customers and orders. In an unnormalized database, the information about a customer and their orders would be stored in a single table. However, this would lead to a lot of redundant data and make it difficult to update customer information. Instead, the data can be split into two tables: one for customers and one for orders. The customer table would store information such as the customer’s name, address, and email, while the order table would store information about each individual order, such as the date of the order and the products purchased.



# STEP 7 : Creating Tables by compress method




# STEP 8: Use Appropriate Data Type

Using appropriate data types is important for optimizing SQL databases. For example, using an integer data type for a column that stores only small positive numbers is more efficient than using a floating-point data type. Similarly, using a fixed-length string data type is more efficient than using a variable-length string data type.

For example, let’s consider a database that stores information about customer orders. If you have a column that stores the quantity of items ordered, you should use an integer data type, as it’s more efficient than afloating-point data type. Similarly, if you have a column that stores customer names, you should use a fixed-length string data type, as it’s more efficient than a variable-length string data type.


# STEP 9 : Partition on Ticket dates

Partitioning is a technique for breaking up a large table into smaller, more manageable pieces.
This can help improve performance by reducing the amount of data that needs to be scanned and processed.

For example, let’s consider a database that stores information about customer orders. If you frequently need to retrieve information about orders
placed in a specific month, you could partition the table based on the order date. This would allow the database to quickly retrieve information about orders placed in a specific month without having to scan the entire table.


# STEP 10 : Indexing on Require Columns to Retrive the data 10x Faster

   Indexing is one of the most important techniques for optimizing SQL databases.
   An index is a data structure that provides quick access to rows in a table based on the 
   values in one or more columns. Without an index, the database would have to scan the entire table to find the data you’re looking for, 
   which can be very slow when dealing with millions of records.
   
For example, let’s consider a database that stores information about customer orders. If you frequently need to retrieve information about orders placed by a specific customer, you could create an index on the customer ID column. This would allow the database to quickly find all the rows that have a specific customer ID without having to scan the entire table.

 


# STEP 11 : Avoiding unnecessary Sub Queries,Distinct,Joins


# STEP 12 : Creating Views

Views are virtual tables that are derived from the data in one or more tables. They can help to simplify the SQL code required to access the data and also provide a level of abstraction from the underlying data.

For example, let’s consider a database that stores information about customer orders. If you frequently need to retrieve information about orders placed by a specific customer, you could create a view that provides a simplified view of the data, with only the relevant columns and only the relevant rows. 
This view could then be used in place of the original table, which would simplify the SQL code required to access the data and also provide a level of abstraction from the underlying data.


# STEP 13 : Creating Store Procedures
Stored procedures are pre-compiled sets of SQL statements that can be executed repeatedly. They can help to optimize SQL databases by reducing the amount of SQL code that needs to be sent over the network and parsed by the database server.

For example, let’s consider a database that stores information about customer orders. If you frequently need to retrieve information about orders placed by a specific customer, you could create a stored procedure that takes the customer ID as a parameter and returns the relevant information. This stored procedure would be stored on the database server, and it would be executed whenever you need to retrieve the information. This would reduce the amount of SQL code that needs to be sent over the network and parsed by the database server, which would help to improve performance.

