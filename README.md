# OpenStreetMap Tileserver
This repository contains instructions for building a
[Docker](https://www.docker.io/) image using [Docker-compose](https://docs.docker.com/compose/), which contains the OpenStreetMap tile
serving software stack.  It is based on the
[Switch2OSM instructions](https://switch2osm.org/serving-tiles/manually-building-a-tile-server-14-04/).

The Docker-compose launches multiple containers which can be found on [Github](https://github.com/VincentDS?tab=repositories) and [Docker Hub](https://hub.docker.com/search/?q=vincentds1&page=1&isAutomated=0&isOfficial=0&starCount=0&pullCount=0). These dockers are based on dockers created by [openfirmware](https://github.com/openfirmware).

# Usage

1. Download an `osm.pbf` file of your favorite region and store it in `~/osm/import.osm.pbf`.
2. Launch docker-compose `docker-compose up -d`. The server will be initialized by storing the map data into the database and subsequently serving the right tiles on `http://my-docker-ip/osmb/{z}/{x}/{y}.png`. 
3. Stop the docker container: `docker-compose stop`
4. Restart the initialized server: `docker-compose start`