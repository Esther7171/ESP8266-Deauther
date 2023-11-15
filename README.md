# ESP8266-Deauther

<p align="center">

<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/d9409805-d8f1-4251-92ee-9837db8e3b72" width="250" height="350" />
</p>

#### ***Scan for WiFi devices, block selected connections, create dozens of networks and confuse WiFi scanners!***


# Why i Prefer This 
<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/e8d70955-7af3-4337-b125-fd3dc6c6d020" width="400" height="200" />
</p>

* As a Hacker it important to increase your skill and Increase the number of tools becouse at sudden time it might be advantageous.
*  This is litreally cheap and small in size and belive me it's a serial killer.
*  Let me give u one such a example: suppose u are in public Cafés and you decided to preform a Deauthentication attack you open up your laptop pluge in your wireless adapter and start deauthenticating people One by One. Now the people will start a suspect and the common suspicion will fall on you because you have a laptop and thier is a weird device connected to your laptop which have some sort of an antina , well you can preform the same using a Nodemcu but this time you will controlling your nodemcu either with your phone or powerbank and that Nodemcu will be hidden inside you pocket taking power from your phone/laptop/powerbank anywhere it just need power to turn on although it illegal to jam networks. but at This point we can use an Nodemcu to kick of people form their network . however the condition is it only supports 2.4 Ghz network but it still good becouse you able to find vunerable device and network at public places. It good for trolling in my perspective.
# Functions
* Scan for WiFi networks and clients
* Create docents of WiFi networks (beacon flooding)
* Confuse WiFi trackers by sending fake probe requests (probe flooding)
* Disconnect selected devices by sending deauth packets (deauthentication attack)
# About this Project
This is an IOT device allows you to easily perform a variety of actions to test networks using an ESP8266. It's also a great project for learning about *WiFi*, *microcontrollers*, *Arduino*, *hacking* and *electronics/programming* in general.
# DISCLAIMER
This project is a proof of concept for testing and educational purposes.
Neither the ESP8266, nor its SDK was meant or built for such purposes. Bugs can occur!
Use it only against your own networks and devices!
Please check the legal regulations in your country before using it.
We don't take any responsibility for what you do with this program.
# How it works
A deauthentication attack works by sending packets that tell the receiver they are disconnected. Deauth frames are a necessary part of the WiFi protocol.
However, these packets are often unprotected. This means that any WiFi device can theoretically craft packets that disconnect nearby connections. 
All they need to know is the sender and receiver address, which can be observed by passivly scanning for WiFi devices.
# NodeMCU
The NodeMCU board is probably the most popular ESP8266 development board. It's cheap, widely available, uses the ESP12 module, and has pre-soldered header pins - which come in handy when using a breadboard.

The original NodeMCU (as seen in the picture above) uses a CP2102 USB serial chip. The NodeMCU V3 is slightly bigger and uses the CH340 chip. However, both versions work the same.

Do not buy an ESP32 version if you're planning to build a Deauther. You'll need an ESP8266! ESP32 is good but it also have its own issues. to be simple leave it here.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/20099b84-cbc1-445b-b4d5-0bce720a5a41" width="400" />
</p>

# Buy
👉 [Amazone](https://www.amazon.in/gp/product/B010O1G1ES/ref=ppx_yo_dt_b_asin_image_o01_s00?ie=UTF8&psc=1)

👉 [Aliexpress](https://www.aliexpress.com/item/1005001636634198.html?aff_fcid=8ca56e73f1ac424eaa4914f7d598c19a-1700053408353-00489-_9gMH6T&tt=CPS_NORMAL&aff_fsk=_9gMH6T&aff_platform=portals-search&sk=_9gMH6T&aff_trace_key=8ca56e73f1ac424eaa4914f7d598c19a-1700053408353-00489-_9gMH6T&terminal_id=478e34abe83644b4b80bc88a122abcdd&afSmartRedirect=y)

# Installation Guide
* Download .bin file of ESP8266.
* Download Flash software given above.
* Connect your ESP8266 board via USB .
* Open Flash software download from above.
* Click Connect and select the serial port of your ESP8266. it is default on com5 or com3 so dont change if it not set it.
* Go to config tap on setting icon Select your Deauther .bin file

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/d2c45c98-a8a3-4943-b17a-da2601b63332" width="600" />
</p>

* Go to operation.
* Tap on flash.
* It take 2-5 min to complete.
* when it finish unpluge and repluge it. 
## TIP
The WiFi password for ```pwned``` is ```deauther``` in case you were looking for it 😉
## Usage
### Connect it to any powersource via USB.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/20221cd2-76bf-434b-9c38-91b16dbfebd0" width="280" />
</p>


### Connet to ESP8266 name of Network.
### Open your browser type this
* 192.168.4.1 [link](192.168.4.1)
* deauth.me
  
<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/185b65b9-ebe1-4352-ac5e-3d1374b60552" width="280" />
</p>

### Click on i understand.
<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/33cd1256-a1a9-4638-b908-0952eaed87fb" width="280" />
</p>

### It auto scan for devices
* Select Networks to Attack
<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/0cb7426c-1336-44d2-9bf6-ff6e9f62867d" width="280" />
</p>

### Top left You find attack tap on that and launch attack as you like
<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/393cb304-0098-41f8-821b-7ec9f9449e8f" width="280" />
</p>

## Reset
To reset you nodemcu use ai thinker reset file given on the top And flash again your deauther code.
### Thank you 🙂
