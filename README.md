## DHT22_ESP32 Sensorbase example
### ESP32
#### this code will do:
1. connect to Wi-Fi router
2. collect measurements
- each measurement contain: Temperature, Humidity
3. sends the measurements as json string to the Gateway

for more information refere and thx to:
https://xylem.aegean.gr/~modestos/mo.blog/esp32-send-dht-to-mqtt-and-deepsleep/

please define all necessary parameter in the script such as:
- Gateway IP
- Wifi logins
- Gpio of one wire connection
- type of DHT (22/11)

## DHT22_RPI Sensorbase example
### RPI 2 - 4 /zero
#### this code will do:
1. connect to Wi-Fi router
2. collect measurements
- each measurement contain: Temperature, Humidity, Time
3. sends the measurements as json string to the Gateway

Install python Module "paho.mqtt" and "Adafruit_DHT".

please define all necessary parameter in the script such as:
- Gateway IP
- Gpio of one wire connection
- type of DHT (22/11)

## weather example
### RPI 2 - 4 /zero
#### this code will do:
1. connect openweather.org
2. get json form api
3. sends velues to the server where it can be displayd in grafana e.g

Install python Module "requests". "paho.mqtt" and "json".
This script is ment to be run on the gateway it self, but you can change it.

!!!You will need an account on openweather.org to get an api_key!!!

please define all necessary parameter in the script such as:
- api_key
- city
- country

## Lux Sensorbase example
### Adafruit Feather m0 Wi-Fi with tsl2591
#### this code will do:

1. connect to Wi-Fi router
2. collect measurements (how many can be defined)
- each measurement contain: lux with timestamp provided by udp server
3. sends the measurements as json string to the Gateway

if the feather is plug to power chare.

 -> Measurement will stop and send. 
 
if the feather is unplugged form power.

 -> measurement will begin

please define all necessary parameter in the script such as:
- Wi-Fi
- Gateway IP

## Radon Sensorbase example
### Raspberry Zero w with RD200M
#### this code will do:

1. connect to Wi-Fi router / Hotspot
2. collect measurements (how many can be defined) from RD200M
- each measurement contain: radon with timestamp provided by udp server + INFO
3. sends the measurements as json string to the Gateway (->Self)

please define all necessary parameter in the script such as:
- Wi-Fi
- and setup a gateway before

## sma_inverter example
### RPI 2 - 4 /zero
#### this code will do:
1. connect to a sma inverter over modbus-tcp
2. get current active power and the Power over the day
3. sends velues to the server where it can be displayd in grafana e.g

Install python Module "socket", "paho.mqtt", "pymodbus" and "json".
This script is ment to be run on the gateway it self, but you can change it.

please define all necessary parameter in the script such as:
- sma_inverter_ip
- sma_inverter_port if needed
- and change hostname if script is not run on gateway it self.


## Bioimpedance analyzer with AD5933 example
### RPI 2 - 4 /zero
#### this code will do:
1. Communicate with an AD5933 impedance analyzer.
2. expand measurement channels up to 32 via two 16 channel MUX.
3. interactive dashboard written in Node-Red.
4. collected data can be stored locally on a USB stick or on the platform via MQTT
5. error checking before measurement included
6. multiple setting options including calibration settings
7. sends data to the server where it can be displayed e.g. in Grafana
8. and much more

node.js Modules "Node-Red"
npm Modules "i2c-bus".
This script is ment to be run on the gateway it self, but you can change it.

