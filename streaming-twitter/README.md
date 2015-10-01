# streaming-twitter

This applications consumes Twitter streams. 

## Configure

Copy the `config.properties.template` to a file called `config.properties`, where you can edit the twitter connection info, the servers used, schema information and filters. 

## Submit the application to Spark

You need to have Spark, Kafka, Zookeper and Schema-registry running.

    ./sbin/spark-submit --class com.ontos.service.ner.FoxProcessor \
    --master spark://localhost:7077 \
    fox-ner-processor-jar-with-dependencies.jar myAppName config.properties