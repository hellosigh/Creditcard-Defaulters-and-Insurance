# Creditcard-Defaulters-and-Insurance
This project helps the Financial institutions such and Insurance and Banking systems understands the 
Creditcard defaulters to define the Insurance premium accordingly, it analyze a wide variety of online 
and offline customer data including the customer transactions, customer master data, insurance data 
etc. Bank can analyze this data to generate insights about individual consumer behaviors and 
preferences. This tool builds the strategies, Key Performance Indicators (KPI) definitions and 
implementation roadmaps that assists our esteemed clients in their Analytics & Information ecosystem 
journey right from Strategy definition to large scale Global Implementations & Support using the bigdata 
ecosystems.
As a part of Enterprise Data lake build, the data will be persisted into Hadoop file system, HBASE and 
Hive are injected using Sqoop for data exchange from DB sources, SFTP/SCP for file transfer from Cloud 
platform. Data transformation and processing such as aggregation, filtering, grouping using Hive for 
Batch data and Phoenix for online data access on Hbase for realtime data aggregation and reporting as 
per the reporting needs.

# Author
-Ramesh Singh- ramesh-kumar.singh@edu.dsti.institute

# Mentors
Gonzalo Etse - gonzaloetjo@gmail.com
Yanis Bariteau - yanis@adaltas.com
Guillaume Holdorf - guillaume.h@adaltas.com

# How to run the project?
Start the Following services:
Hadoop:
start-all.sh
mr-jobhistory-daemon.sh start historyserver
# Login, start mysql service and exit: 
service mysqld start
sudo mysql -u root -p
password: root
# Data preparation in the source systems
  DB to Hadoop Data Ingestion:
  Insert into the mysql database - custmaster data in a table and the credit data into 2 tables of 2 
# Sqoop integration with Hive + ETL & ELT operations (Merge the 2 dataset using Hive and split the 
defaulters and non-defaulters into 2 data sets and load into hdfs. )
# Import the creditcard datasets of cst and pst timezones into hive table with the below given steps.
1. Create a database in hive as insure.
create database if not exists insure;
2. Sqoop import the data into hive table insure.credits_pst and insure.credits_cst with options 
such as hive overwrite, number of mappers 2, where hive table created by sqoop with id as 
bigint, billamt as float

# ETL & ELT using Hive
Create a hive table with header line count as 1 and load the insurance dataset. 
hive --service metastore
hive
create database if not exists insure;
use insure;
# Data Provisioning using Hive, Sqoop and DistCp
1 Insert into the mysql database - custmaster data in a table and the credit data into 2 tables of 2 
timezones:
2 Import the creditcard datasets of cst and pst timezones into hive table
3 Sqoop import the data into hive table insure.credits_pst and insure.credits_cst with options 
such as hive overwrite, number of mappers 2, where hive table created by sqoop with id as 
bigint, billamt as float




