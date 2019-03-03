
# Original Github

This is forked from [gettyimages](https://github.com/gettyimages/docker-spark)

# About

A `debian:stretch` based [Spark](http://spark.apache.org) container. Use it in a standalone cluster with the accompanying `docker-compose.yml`, or as a base for more complex recipes.

## Why

I want to get familiar with Spark, and didn't want to have to install Spark. So I found myself a nice docker instance and started to play around. 

I wrote a very [brief blog post](https://dabble-of-devops.com/getting-familiar-with-spark-using-docker/) about the process.

## Run

Bring up the docker-compose instance

    docker-compose up -d
    docker-compose exec master bin/run-example SparkPi 10
    docker-compose exec master python /tmp/data/sort.py /tmp/data/sort_this

Spark has a super nice web UI. For this compose instance its up at http://localhost:8090/.  If you ran the code above you should see two completed applications, one 'PythonSort' and one 'Spark Pi' job.

## license

MIT
