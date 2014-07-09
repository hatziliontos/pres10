pres10
======
A simple web server-client application to remotely monitor some critical system parameters.
A Raspberry Pi Model B plays the role of a web server which is constantly monitoring pressure values of a piezoelectric sensor.
The sensor is connected to a Lantronix xsenso 4-20mA converter.
Both RaspB+Lantronix belong to the same local ethernet subnetwork.
Code inside RaspB is a node.js file which performs specific cyclic operations.
