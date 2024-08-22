# NodeRed
This are samples in NodeRed plus a docker-compose.yml for a simpler test environment

The docker compose is configured to run with a Raspberry 4 ( Got it also running on a version 3 )
Origin of all ist the IOTstack project. It contains a lot of usefull documentation in its wiki. If you do not know, read it.

The MQTT brocker for the IOT devices is called mosquitto.
From this node-red extracts to different customers
  1. His own node-red ui = host:1880/ui
  2. Data is written into InfluxDB
  3. A second mqtt brocker with the name fuxamosq gets condensed data
As a SCADA application FUXA reads from this fuxamosq broker = host:1881  ( The fuxa implementation is a work in progress, can read already... )
Finally the container can be controlled via portainer_ce.

The big version of NodeRed jsons is intended to run on the rpi. It contains beside 10 M5Stack-C3U devices and one ESP32-2432S024N also a collection of my shelly implementation.
Plus some network and RPI system monitoring.

At last there is a small NodeRed that can run on your programming device. It is flodding the IOT-broker with random data.

Have fun!
