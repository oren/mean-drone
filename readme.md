# MEAN.JS with Drone.io

MEAN.JS, Drone.io and Docker

Run tests on each push to master.

![drone.io in action](drone.png)

* [Run](#run)
* [Develop](#develop)
* [Test Drone](#test-drone)
* [Setup Drone](#setup-drone)

## Run (using docker, daemonized)

    fig up
    open 0.0.0.0:3000

## Develop (using docker)

    ./scripts/dockerize
    ./scripts/start        # run this inside the container
    open 0.0.0.0:3000

## Test drone

    drone build

