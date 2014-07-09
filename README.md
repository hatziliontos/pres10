pres10
======
A simple web server-client application to remotely monitor some critical system parameters.
A Raspberry Pi Model B plays the role of a web server which is constantly monitoring pressure values of a piezoelectric sensor, installed on a municipal water distribution pipe.
The sensor is connected to a Lantronix xsenso 4-20mA converter.
Both RaspB+Lantronix belong to the same local ethernet subnetwork.
Code inside RaspB is a node.js file which performs specific cyclic operations.

User Interface
======
Client operations are implemented by a few html files. The central file frames.html constructs user interface which consists of four frames, top_nav.html a navigation frame located on the top of screen, local_history.html a navigation frame located on the left of screen,  
