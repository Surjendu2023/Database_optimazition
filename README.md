# ETL_with_database_optimazition

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
           
           
           


           

           
           
          
                    
