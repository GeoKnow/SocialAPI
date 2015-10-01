## Configure

Copy the `config.properties.template` to a file called `config.properties`, where you can edit the topics to consume connection info, the servers used, schema information and filters. 

## Requirements

TODO: describe the type od the topics thisc comsume/uses AvroDeserialization


## Submit the application to Spark

You need to have Spark, Kafka, Zookeper and Schema-registry running.

    spark-submit --class com.ontos.spark.serializer.rdf.RdfSerializer \
    --master spark://localhost:7077 \
    rdf-serializer-jar-with-dependencies.jar myAppName config.properties

