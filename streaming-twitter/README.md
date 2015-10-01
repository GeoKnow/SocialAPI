# streaming-twitter

This applications consumes Twitter streams. 

## Download

Since Github has a file size limit it was not possible to put here the binaries. But you can download it form here:
http://generator.geoknow.eu/social-api/streaming-twitter-jar-with-dependencies.jar

## Configure

Copy the `config.properties.template` to a file called `config.properties`, where you can edit the twitter connection info, the servers used, schema information and filters. 

## Submit the application to Spark

You need to have Spark, Kafka, Zookeper and Schema-registry running.

    ./sbin/spark-submit --class com.ontos.service.ner.FoxProcessor \
    --master spark://localhost:7077 \
    fox-ner-processor-jar-with-dependencies.jar myAppName config.properties