# Sensor
Wir wollen hier Methodik zur Referenzmessungen bereitzustelen um die Genauighkeit von verschidenen Systemen zu untersuchen.
## Zugriff auf die Messungen
Der Zugriff auf die Messungen kann auf mehrere Arten erfolgen. 
### Daten unter ROS bzw. MAVROS
Im Rossystem gibt es ein MAVROS Bibliothek die alle benötigten Werkzeuge beinhaltet, mit dem Vorteil des Zeitstempels.
ROS verwendet ein "Publisher-Listener" Konzept welches darauf basiert dass ein sogenanntes "Topic" initialisiert wird und in diesen Topic veröffentlicht der Publisher die Daten welche mit dem Listener abgefragt werden Können. Die Topics mit den Sensordaten werden automatisch mit MAVROS initialisiert. Zum abrufen der Daten muss man unter ROS folgendes Konstrukt benutzen:

rostopic echo /mavros/imu/data

oder einen Listener in C++ oder Python schreiben um die Daten weiter zu verarbeiten. Ein Beispiel für ein Listener und Publisher kann in catkin_ws/scripts/MAVROS nachgeschlagen werden.

http://ardupilot.org/dev/docs/ros.html
### Daten unter PYMAVLINK / DroneKit
Hier verbinden wir uns per MAVLINK direkt mit der Drohne ohne dem Umweg über ROS. Diese Methode ist ohne Zeitstempel und Synchronisation deswegen nicht genauer erläutert. Für mehr Informationen:

https://dev.px4.io/en/middleware/mavlink.html

https://dev.px4.io/en/robotics/dronekit.html
## Non-GPS Navigation
http://ardupilot.org/copter/docs/common-non-gps-navigation.html
### Optial Flow
https://docs.px4.io/en/sensor/px4flow.html

http://ardupilot.org/copter/docs/common-px4flow-overview.html

#### PX4FLOW

Specifications:

    168 MHz Cortex M4F CPU (128 + 64 KB RAM)
    752×480 MT9V034 image sensor, L3GD20 3D Gyro
    16 mm M12 lens (IR block filter)

Features:

    MT9V034 machine vision CMOS sensor with global shutter
    Optical flow processing at 4×4 binned image at 120 (indoor) to 250 Hz (outdoor)
    Superior light sensitivity with 24×24 μm super-pixels
    Onboard 16bit gyroscope up to 2000°/s and 780 Hz update rate, default high precision-mode at 500°/s
    Onboard sonar input and mount for Maxbotix sonar sensors. PX4 Flow comes with the sonar already mounted and installed. MB1043
    USB bootloader
    USB serial up to 921600 baud (including live camera view with QGroundControl)
    USB power option


http://ardupilot.org/copter/docs/common-optical-flow-sensors-landingpage.html#common-optical-flow-sensors-landingpage

#### Cheerson CX-OF Optical Flow
    The Cheerson CX-OF optical flow sensor is a leightweight and low cost optical flow sensor which can be used to improve horizontal position control especially in GPS denied environments.
## GPS
TODO
## IMU
TODO
## AruCo feat. RPi mit Kamera
TODO
