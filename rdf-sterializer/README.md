# rdf-serializer

This Spark application serialises Kafka messages with rdf content into the HDFS or to a RDFStore.


## Download

Since Github has a file size limit it was not possible to put here the binaries. But you can download it form here:
[http://generator.geoknow.eu/social-api/rdf-serializer-jar-with-dependencies.jar](http://generator.geoknow.eu/social-api/rdf-serializer-jar-with-dependencies.jar)

## Requirements

This applications consumes Avro messages that are in the [format](https://github.com/GeoKnow/SocialAPI/blob/master/fox-extractor/ner-rdf-schema.json) provided by the [fox-extractor](https://github.com/GeoKnow/SocialAPI/tree/master/fox-extractor) application.


## Configure

Copy the `config.properties.template` to a file called `config.properties`, where you can edit the topics to consume connection info, the servers used, schema information and filters. 


## Submit the application to Spark

You need to have Spark, Kafka, Zookeper and Schema-registry running.

    spark-submit --class com.ontos.spark.serializer.rdf.RdfSerializer \
    --master spark://localhost:7077 \
    rdf-serializer-jar-with-dependencies.jar myAppName config.properties

