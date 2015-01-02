# MEAN.JS with Drone.io

MEAN.JS, Drone.io and Docker

Run tests on each push to master.

* [Run](#run)
* [Develop](#develop)
* [Test Drone](#test-drone)
* [Setup Drone](#setup-drone)

## Run (using docker, daemonized)

    fig up
    open 0.0.0.0:3000

## Develop (using docker)

    docker run -d --name db mongo
    docker build -t mean .
    docker run -it --rm -p 3000:3000 -v $(pwd):/home/mean --link db:mean_db_1 --name mean-app mean /bin/bash
    npm install
    bower install --allow-root
    grunt test
    grunt
    open 0.0.0.0:3000

## Test drone

    drone build

