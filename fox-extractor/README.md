# fox-extractor

This applications consumes kafka messages of a given topic and process its content with FOX. 

## Configure

Copy the `config.properties.template` to a file called `config.properties`, where you can edit the twitter connection info, the servers used, schema information and filters. 

## Submit the application to Spark

You need to have Spark, Kafka, Zookeper and Schema-registry running.

		./bin/spark-submit --class com.ontos.spark.streaming.twitter.SparkTwitterApp --master spark://localhost:7077 target/streaming-twitter-jar-with-dependencies.jar config.properties