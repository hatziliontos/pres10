pres10
======
A simple web server-client application to remotely monitor some critical system parameters.
A Raspberry Pi Model B plays the role of a web server which is constantly monitoring pressure values of a 0-10bar piezoelectric sensor, installed on a municipal water distribution pipe.
The sensor is connected to a Lantronix xsenso 4-20mA converter.
Both RaspB+Lantronix belong to the same local ethernet subnetwork.
Code inside RaspB is a node.js file which performs specific cyclic operations.

User Interface
======
Client operations are implemented by a few html files. The central file frames.html constructs user interface which consists of four frames, top_nav.html a navigation frame located on the top of screen, local_history.html a navigation frame located on the left of screen, gauge.html a value indicating gauge located on the top right of screen and content.html a central displaying frame located on the center of screen.

top_nav.html
======
top_nav.html gives user 5 hot link options, Επιτήρηση Αρχείου (local_history.html), Service (service.html), Σχετικά (about.html), Βοήθεια (help.html), Ανακοινώσεις (newsletter.html). Above the options there is an informative application title (Συνεχής Επιτήρηση Υδραυλικής Πίεσης Καλλικράτειας) and the server IP network address (internet plus intranet IP). User can also watch the current measured water pressure value.

gauge.html
======
gauge.html is a special Google Gauge and simulates the pump manometer gauge operation. Displayed ranges are divided in 3 colored ranges, low - medium - high pressure range.

content.html
======
![frames](https://cloud.githubusercontent.com/assets/6866345/3530270/e78114a2-07a2-11e4-91fb-82e6c30b150d.png)
It simply displays a Google Line Chart with the last recorded pressure values. Chart is refreshing every 10-20 sec.

local_history.html
======
![tilnowchart](https://cloud.githubusercontent.com/assets/6866345/3530378/d506440e-07a3-11e4-82ca-3de9c7aebb79.png)
After selecting Επιτήρηση Αρχείου->Μετρήσεις 24ωρου the user is able to watch current day recorded values.
![dirtxt](https://cloud.githubusercontent.com/assets/6866345/3530726/939313b8-07a7-11e4-9e3b-50060dc31cb4.png)
After selecting Επιτήρηση Αρχείου->Ημερήσια Αρχεία the user is able to watch files with daily records.
![resultsrecord](https://cloud.githubusercontent.com/assets/6866345/3530923/ea6a0924-07a9-11e4-8b84-875280b8badc.png)
After selecting Επιτήρηση Αρχείου->Ημερήσια Αρχεία->linked file the user is able to watch the table with this day records.
