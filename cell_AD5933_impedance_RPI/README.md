# cell_AD5933_impedance
Node red flow and installation method for an impedance measurement in a 24-well microtiter plate using the AD5933 impedance analyzer.


### insatlation
This node red flow anable an RPI to communicate with the AD5933 impedance analyzer and two 16-channel MUX to measure impedance in a microtiter plate.
The collected data can be stored on a USB stick or passed on to an IoT platform, or both. 
To do this, the following nodes must be installed to the defult nodes (rpi):
- npm install node-red-dashboard
- npm install node-red-contrib-mqtt-connection-check
- npm install node-red-contrib-i2c

Second, the npm module "i2c-bus" must be loaded as an external module to work in the function node:
to do this:
- if not installed, go to ~/.node-red and install with "npm install i2c-bus i2c".
- then go to settings.js and add under functionGlobalContext add:
        os:require('os'),
        ic:require('i2c-bus'),
- reload node-red with: sudo "systemctl restart node-red".


### NOTE:
Then everything should work and the measurement network can start by setting the parameter on the dashabord.
For sending the data via MQTT the gatway must be installed on the same device.

### Image of the first prototype
3D pritited cover with gold electrodes conected to the two 16 channel MUX and the AD5933 (from PMODIA DIGILENT)
![alt text](https://github.com/IoTree/cell_AD5933_impedance/blob/main/Prototype.jpg)
