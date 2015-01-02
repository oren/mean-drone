# MEAN.JS with Drone.io

MEAN.JS, Drone.io and Docker

* [Run](#run)
* [Develop](#develop)

## Run (using docker)

    fig up
    open 0.0.0.0:3000

## Develop (using docker)

    docker run -d --name db mongo
    docker build -t mean .
    docker run -it --rm -v $(pwd):/home/mean --link db:mean_db_1 --name mean-app mean /bin/bash
    npm install
    grunt test
    grunt
    open 0.0.0.0:3000
