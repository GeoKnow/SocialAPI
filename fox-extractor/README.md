# fox-extractor

This applications consumes kafka messages of a given topic and process its content with FOX. 

## Download

Since Github has a file size limit it was not possible to put here the binaries. But you can download it form here:
[http://generator.geoknow.eu/social-api/ner-fox-jar-with-dependencies.jar](http://generator.geoknow.eu/social-api/ner-fox-jar-with-dependencies.jar)

## Requirements

This applications consumes Avro messages that are in the [format](https://github.com/GeoKnow/SocialAPI/blob/master/streaming-twitter/tweet-schema-with-topic.json) provided by the [streaming-twitter](https://github.com/GeoKnow/SocialAPI/tree/master/streaming-twitter) application.

## Configure

Copy the `config.properties.template` to a file called `config.properties`, where you can edit the twitter connection info, the servers used, schema information and filters. 

## Submit the application to Spark

You need to have Spark, Kafka, Zookeper and Schema-registry running.

		./bin/spark-submit --class com.ontos.service.ner.FoxProcessor \
		--master spark://localhost:7077 \
		fox-ner-processor-jar-with-dependencies.jar myAppName config.properties