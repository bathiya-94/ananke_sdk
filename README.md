# Ananke IoT Platform



Ananke is developed by Effective Solutions Pvt Ltd as an end to end cloud based IoT platform. Ananke delivers amazing set of features for IoT developers which enable connecting IoT hardwares, applications and services together. Ananke follows platform as a service model with following features,

*Multi-protocol support (MQTT,Web Sockets and HTTP)

*Cloud services for Machine Learning and Logic Processing

*Cloud APIs for Smart Transportation, Health Care, etc

*Easy prototyping with complete graphical programming interface.

*SDK availability for Raspberry Pi, Arduino and other iot enabled developer kits

# Ananke SDK 1.0.0v
The purpose of this SDK is to connect Raspberry Pi devices to Ananke platform. Ananke recognizes a device with following parameters (please refer the Ananke User Manual to learn more).

*Device Username

*Device Password

*Device App Id

*Device Group Id

*Device Id

The SDK enable you to simply connect your device to Ananke with the above parameters. The communication with the platform is handled by the events for connection initiation, message receiving and a simple method to send messages to the platform. You can connect your device to many other internet of things using the routing layer.


# Installation

Open your terminal and navigate to the project folder.Make  sure that you have npm installed in your computer. Then type the following command in your terminal:


```
$npm install ananke_sdk
```
# Usage

To begin the connection:
```
const sdk = require(‘ananke_sdk’');
var mySdk=sdk(options);
mySdk.begin(Onconnect,OnMessage);

```
To send a message:

```
const sdk = require(‘ananke_sdk’');
var mySdk=sdk(options);
mySdk.sendMessage(message);

```

# Sample Code

```
const sdk = require(‘ananke_sdk’');

var options = {
  		 appId: 'a1476238',
   		groupId: 'g2349178',
   		deviceId: 'd4083171',
   		username: 'bathi1',
  		 password: '1234'
}

var mySdk = sdk(options);
messageapp2='app 2 on connect message.';


if(mySdk != null){

 mySdk.begin(onConnect,onMessage);

}

```




