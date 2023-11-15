# ESP8266-Deauther
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/d9409805-d8f1-4251-92ee-9837db8e3b72" width="250" height="350" />

#### Scan for WiFi devices, block selected connections, create dozens of networks and confuse WiFi scanners!

## Why i Prefer This 
let take an exmaple :

you visted a Cafés then you take out your laptop and  your wireless adapter to it and start disconnecting people to the network it take time and 
the first doubt of people is obivousally came on to you becouse you have a laptop and a wired antina on it although it illegal to jam networks. 
but at This point we can use an Nodemcu to kick of people form their network . however the condition is it only supports 2.4 Ghz network but it still good 
becouse you able to find vunerable divice and network at public places. It good for trolling in my perspective.
## Functions
* Scan for WiFi networks and clients
* Create docents of WiFi networks (beacon flooding)
* Confuse WiFi trackers by sending fake probe requests (probe flooding)
* Disconnect selected devices by sending deauth packets (deauthentication attack)
## About this Project
This allows you to easily perform a variety of actions to test networks using an ESP8266. 
It's also a great project for learning about WiFi, microcontrollers, Arduino, hacking and electronics/programming in general.
its easy to use and Sometime you can use it for trolling people at public places by disconnecting them to the network they connected
## DISCLAIMER
This project is a proof of concept for testing and educational purposes.
Neither the ESP8266, nor its SDK was meant or built for such purposes. Bugs can occur!
Use it only against your own networks and devices!
Please check the legal regulations in your country before using it.
We don't take any responsibility for what you do with this program.
## How it works
A deauthentication attack works by sending packets that tell the receiver they are disconnected. Deauth frames are a necessary part of the WiFi protocol.
However, these packets are often unprotected. This means that any WiFi device can theoretically craft packets that disconnect nearby connections. 
All they need to know is the sender and receiver address, which can be observed by passivly scanning for WiFi devices.
## NodeMCU
The NodeMCU board is probably the most popular ESP8266 development board. It's cheap, widely available, uses the ESP12 module, and has pre-soldered header pins - which come in handy when using a breadboard.

The original NodeMCU (as seen in the picture above) uses a CP2102 USB serial chip. The NodeMCU V3 is slightly bigger and uses the CH340 chip. However, both versions work the same.

Do not buy an ESP32 version if you're planning to build a Deauther. You'll need an ESP8266!

<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/20099b84-cbc1-445b-b4d5-0bce720a5a41" width="400" />

## Buy
👉 [ESP8266](https://www.amazon.in/gp/product/B010O1G1ES/ref=ppx_yo_dt_b_asin_image_o01_s00?ie=UTF8&psc=1)

👉 [ESP8266](https://www.aliexpress.com/item/1005001636634198.html?aff_fcid=8ca56e73f1ac424eaa4914f7d598c19a-1700053408353-00489-_9gMH6T&tt=CPS_NORMAL&aff_fsk=_9gMH6T&aff_platform=portals-search&sk=_9gMH6T&aff_trace_key=8ca56e73f1ac424eaa4914f7d598c19a-1700053408353-00489-_9gMH6T&terminal_id=478e34abe83644b4b80bc88a122abcdd&afSmartRedirect=y)

## Installation Guide
* Download .bin file of ESP8266.
* Download Flash software given above.
* Connect your ESP8266 board via USB .
* Open Flash software download from above.
* Click Connect and select the serial port of your ESP8266. it is default on com5 or com3 so dont change if it not set it.
* Go to config tap on setting icon Select your Deauther .bin file
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/d2c45c98-a8a3-4943-b17a-da2601b63332" width="600" />

* Go to operation.
* Tap on flash.
* It take 2-5 min to complete.
* when it finish unpluge and repluge it. 
## TIP
The WiFi password for ```pwned``` is ```deauther``` in case you were looking for it 😉
## Usage
* Connect it to any powersource via USB.
* Connet to Network.
* type on your browser deauther.me / 192.168.4.1
* Click on i understand.
* Done !
## Support 
To reset you nodemcu use ai thinker reset file given on the top And flash again your deauther code.
### Thank you 🙂
