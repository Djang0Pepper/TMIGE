#####################################
            T M I G e
    Tasmota MQTT Influxdb Grafana
#####################################

This repository provides a starting point for wiring up an IoT-device running Tasmota_ to an InfluxDB_ over MQTT_ and
displaying the results in Grafana_.

The rendered guide can be found at `<https://svalouch.github.io/tasmota-python-mqtt-influxdb-grafana-example/>`_

My modifications are for DS18B20(4K7 and GPIO3) and DHT(AM2301 GPIO2) on a simple ESP01

[Unit]
 2 Description=Tasmota Mqtt Influx Graphan python bridgE
 3 After=network.target
 4
 5 [Service]
 6 Type=simple
 7 ExecStart=/usr/bin/python /usr/local/bin/TMIGE.py
 8 WorkingDirectory=/home/pi/TMIGE
 9 StandardError=syslog
10 Restart=always
11 User=pi
1215 Restart=always
16
17 [Install]
18 WantedBy=multi-user.target

