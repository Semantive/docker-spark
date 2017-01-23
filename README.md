# semantive/spark

An [Apache Spark](http://spark.apache.org) container based on `openjdk` image. Use it in a standalone cluster with the accompanying `docker-compose.yml`, or as a base for more complex recipes.

## Simple example

To run `SparkPi`, run the image with Docker:

    docker run --rm -it -p 4040:4040 semantive/spark bin/run-example SparkPi 10

## Cluster example [docker-compose]

To create a simple standalone cluster with [docker-compose](http://docs.docker.com/compose) use:

    docker-compose up

The SparkUI will be running at `http://${YOUR_DOCKER_HOST}:8080` with one worker listed and Spark jobs may be submitted using master `spark://${YOUR_DOCKER_HOST}:7077`. To connect via spark-shell with cluster use:

    spark-shell --master spark://localhost:7077

## License

Apache Licence
