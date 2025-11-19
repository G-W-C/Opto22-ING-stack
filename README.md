# Opto22-ING-stack

##### This tutorial is for creating an open source historian using Opto22 Hardware, Node-Red, influxDBv2, and Grafana

The docker-compose.yml is configured for users running Node-RED on the groov EPIC.
###### For SNAP-PAC users (without and EPIC) can add Node-RED to the docker-compose.yml

* Download the docker-compose.yml and nignx.conf to the same project directory.
* Open a terminal in the project directory and run the following
  ```
  docker copmose up -d
  ```
* Navigate to:
  * Grafana: http://localhost
  * InfluxDB: http://localhost:8086
