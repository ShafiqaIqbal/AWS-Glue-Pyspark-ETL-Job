# AWS-Glue-Pyspark-ETL-Job
This is a Glue ETL job, written in pyspark, which partitions data files on S3 and stores them in parquet format. This ETL is part of [Medium Article](https://medium.com/p/3a8a24cfa4af/edit) and it is scheduled after [Glue Python-Shell](https://github.com/ShafiqaIqbal/SFTP-S3-Glue-Ingestion-Python) job has dumped filed on S3 from file server. This python-shell job is pre-requisite of this Glue job. Here, I am using [this dataset](https://www.kaggle.com/currie32/crimes-in-chicago). For more information, please go to my article. 

This Glue job provides the following:
* Loads files from S3 into dynamic frames
* Converts the Dynamic Frame into Dataframe
* Renames columns with spaces and unsupported characters 
* Creates partitioning columns
* Repartition files by days and saves data in S3 bucket /year=/month=/ partitioning scheme.
* Stores the partitioned files in parquet files
