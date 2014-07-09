pres10
======
a simple web server-client application to remotely monitor some critical system parameters.
a raspberry pi model B plays the role of a web server which is constantly monitoring the pressure values of a piezoelectric sensor.
the sensor is connected to a Lantronix xsenso 4-20mA converter.
both rasc+Lantronix belong to the same local ethernet subnetwork.
code inside raspberry is a node.js file which performs specific periodic operstions.
