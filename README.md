# SocialAPI
This project contains several application for consuming and processing Twitter streams for the Supply Chain use case in the [GeoKnow](http://geoknow.eu) project.

## Contents

This projects contains three Spark applications for:

- streaming-twitter: Twitter streaming extrtaction
- fox-extractor: Name Entity Recognition extraction that consumes tweets extracted in the streaming-twitter that uses [FOX](https://github.com/AKSW/FOX)
- rdf-storage: a persistance component for saving results form the fox-extractor  


## Requirements

To use these applications you need to have installed and running:

- [Confluent Platform](http://www.confluent.io/)
- [Spark 1.4.1](http://spark.apache.org/)

## Configuration and Testing

You need to configure Spark to have at least three workers available (one for each application). Submit each of the applications to spark using spark-submit (check the README on each of the directories).


## Licence

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/80x15.png" /></a><br/>
<span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">The GeoKnowSocialAPI</span>, a work at <a xmlns:dct="http://purl.org/dc/terms/" href="https://github.com/GeoKnow/SocialAPI" rel="dct:source">https://github.com/GeoKnow/SocialAPI</a> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://www.ontos.com/" property="cc:attributionName" rel="cc:attributionURL">OntosAG</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">Creative Commons Attribution-NonCommercial 4.0 International License</a>.<br />



