# Toronto Apache Spark 
## Rubikloud
Rubikloud is a company that tries to apply AI to retail, promotion management and customer lifecycle management

Terraform 
they have ml engineer, cloud infrastructure engineers, software engineers and data scientists

Talk: Productionizing Machine leaerning
Delta - Koalas - MLflow

You will need to use several technologies to do what you want usually

Kafka

Spark helps a lot as it allows you to do data science and data engineering, and since it has a lot of support there is support for most ml frameworks

On the cloud, with big data there is no schema enforcement, lack of consistency and failed production jobs leave data in a corrupted state requiring tedious recovery

Schema on read

kafka is a streaming thing, so it is not suited for batch

Delta lake solves many problems with data lakes

Spark can aggregate json files

Data lake schemas are stored as parquet files (Apache Parquet)

Data lake architecture
Bronze is raw ingestion
Silver is filtered cleaned and augmented data
Gold is business level aggregates

Data streaming is most cost effective

Summary of the key characteristics
 1. Adopt a continuous data flow model to unify batch and streaming
 2. Use intermediate hops to improve reliability ad troubleshooting
 3. Make the cost vs latency trade off based on your use cases and business needs
 4. Optimize the storage layout based on the access patterns
 5. Reprocess the historical data as needed by simply cleaning the result table and restarting the stream
 6. Incrementally improve the quality of your data until it is ready for consumption with schema management option and data expectations

https://delta.io

Pandas vs PySpark

PySpark is distributed and thus it is more useful for large datasets

Koalas is a merging of the two, if the data is small then under the hood it is going to be a pandas dataframe and with a large dataset it will use PySpark

https://github.com/databricks/koalas

Programming in skala by martin orderski

October 24 or something there will be another databricks meetup





