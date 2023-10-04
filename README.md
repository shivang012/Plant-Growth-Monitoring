# Plant-Growth-Monitoring

Here we are proposing a system to monitor plant health status by measuring the Soil
moisture, Humidity & Temperature and Light intensity using respective sensors, and
monitor the data using cloud based android software application.

Aim: To monitor plant health status by measuring the Soil moisture, Humidity &
Temperature and Light intensity using respective sensors, and monitor the data using
android application.

 Objectives:
 To measure dryness in soil, humidity and temperature and light intensity using soil
moisture sensor, humidity and temperature sensor and light intensity sensor
respectively.
 To send the measured data from the respective sensors to Cloud server, using cloud
software, to monitor them and to keep track of the land condition, using android
application.

 To allow users to have access to the data through their smartphones and to inform them
if there are any deviations with respect to temperature, humidity, soil moisture and light
intensity.

List of Components/Software/Tools Used 

HARDWARE:

Soil Moisture Sensor (YL-38 + YL-69),
Humidity & Temperature Sensor (DHT 11),
Light intensity sensor (TEMT6000),
Wi- fi shield NODE MCU ESP8266,
Jumper wires.

SOFTWARE:

Arduino IDE Software,
Compiler for Arduino program,
Blynk Cloud Software

OTHER COMPONENTS :

Test setup with two cups of soil

Working Methodology 

1. DTH11 will monitor temperature and humidity, YL-38+YL-69 will monitor soil
moisture. These sensors will gather environment information and send the information
to Arduino dev board.

2. The system is connected to IoT based cloud platform known as Blynk cloud using
NODEMCU Wi-Fi shield.

3. In order to exchange data from Node Mcu to other external systems, Arduino Rest API,
is an api provided by the Arduino ide that will read and send information to Arduino
board. It will retrieve sensor values.

4. Blynk cloud platform also uses Arduino Rest API mechanism, by using this
mechanism, when client sends a request, Arduino replies with some data.

5. Arduino Rest API works over HTTP protocol plays an important role in a client server
scenario where Arduino acts as a server.

6. Arduino Rest API uses a library called aRest.. Using the library we can implement
Arduino Rest API model because it supports reading pin values and writing pin values.
Sensor values are stored in NODEMCU.

7. Now we need to configure the Blynk so that the Nodemcu client can send data. This
can be done using Blynk web interface.

8. While configuring the cloud, variable id’s and authentication token are created. Using
authentication token Blynk establishes a connection to the cloud.

9. Arduino HTTP client sends each sensor value assigned with a variable id using JSON
(Java Script Object Notation) service.

10. Then the data is stored in cloud and analyzed. Blynk will allow users to create a
dashboard and to represent stored data as graph.

11. Once the data, like sensor values, is stored in the cloud, it is possible to access it using
smart phones remotely.
