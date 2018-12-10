# Sensor
Wir wollen hier Methodik zur Referenzmessungen bereitzustelen um die Genauighkeit von verschidenen Systemen zu untersuchen.
## Zugriff auf die Messungen
Der Zugriff auf die Messungen kann auf mehrere Arten erfolgen. 
### Daten unter ROS bzw. MAVROS
Im Rossystem gibt es ein MAVROS Bibliothek die alle benötigten Werkzeuge beinhaltet, mit dem Vorteil des Zeitstempels.
ROS verwendet ein "Publisher-Listener" Konzept welches darauf basiert dass ein sogenanntes "Topic" initialisiert wird und in diesen Topic veröffentlicht der Publisher die Daten welche mit dem Listener abgefragt werden Können. Die Topics mit den Sensordaten werden automatisch mit MAVROS initialisiert. Zum abrufen der Daten muss man unter ROS folgendes Konstrukt benutzen:

rostopic echo /mavros/imu/data

oder einen Listener in C++ oder Python schreiben um die Daten weiter zu verarbeiten. Ein Beispiel für ein Listener und Publisher kann in catkin_ws/scripts/MAVROS nachgeschlagen werden.
### Daten unter MAVLINK
## PX4Flow
https://docs.px4.io/en/sensor/px4flow.html
## GPS
TODO
## IMU
TODO
## AruCo feat. RPi mit Kamera
TODO
