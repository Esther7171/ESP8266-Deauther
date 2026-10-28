# ESP8266 Deauther

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/d9409805-d8f1-4251-92ee-9837db8e3b72" width="250" height="350" />
</p>

#### Scan for WiFi devices, disconnect selected clients, spin up dozens of fake networks, and confuse WiFi scanners, all from a NodeMCU.

An ESP8266 (NodeMCU) flashed with deauther firmware. I use it to study 802.11 management-frame attacks (deauthentication, beacon flooding, probe flooding) from the attacker's side, so I can recognise them in the wild and defend against them. It works on 2.4GHz WiFi only.

## The cafe scene

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/e8d70955-7af3-4337-b125-fd3dc6c6d020" width="400" height="200" />
</p>

A cafe at rush hour. One by one, phones drop off the WiFi and scramble to reconnect, and nobody looks up, because there is nothing to see. No laptop, no antenna. Just a board the size of a thumb, running off a power bank, quietly sending 802.11 deauth frames across the 2.4GHz band.

That picture is why this board is worth understanding. It is cheap, tiny, and battery powered, and most people would never spot the source. I built this to learn that threat from the inside: how the frames work, how to catch the attack, and how to shut it down. Everything here is for my own networks and my own lab.

## Functions
* Scan for WiFi networks and clients
* Create dozens of fake WiFi networks (beacon flooding)
* Confuse WiFi trackers with fake probe requests (probe flooding)
* Disconnect selected devices with deauth packets (deauthentication attack)

## How a deauth attack works
A deauthentication attack sends frames that tell a client it has been disconnected. Deauth frames are a normal part of the WiFi protocol, but before WPA3 they are unprotected: any nearby device can craft one once it has seen the sender and receiver addresses, which a passive scan reveals. That is the whole trick.

## How to defend against it
* **802.11w (Protected Management Frames / PMF):** signs management frames, so spoofed deauths are ignored. Mandatory on WPA3, optional on WPA2.
* **A wireless IDS** such as Kismet or nzyme flags a deauth or beacon flood the moment it starts.
* **Move critical devices to 5GHz and WPA3.** A 2.4GHz-only ESP8266 cannot reach them.

## Hardware: NodeMCU
The NodeMCU is the most popular ESP8266 board: cheap, widely available, built on the ESP-12 module, with pre-soldered headers that are handy on a breadboard. The original uses a CP2102 USB-serial chip; the V3 is slightly bigger and uses a CH340. Both work the same. You need an ESP8266 for this, not an ESP32.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/20099b84-cbc1-445b-b4d5-0bce720a5a41" width="400" />
</p>

### Buy
* [Amazon](https://www.amazon.in/gp/product/B010O1G1ES/ref=ppx_yo_dt_b_asin_image_o01_s00?ie=UTF8&psc=1)
* [AliExpress](https://www.aliexpress.com/item/1005001636634198.html?aff_fcid=8ca56e73f1ac424eaa4914f7d598c19a-1700053408353-00489-_9gMH6T&tt=CPS_NORMAL&aff_fsk=_9gMH6T&aff_platform=portals-search&sk=_9gMH6T&aff_trace_key=8ca56e73f1ac424eaa4914f7d598c19a-1700053408353-00489-_9gMH6T&terminal_id=478e34abe83644b4b80bc88a122abcdd&afSmartRedirect=y)

## Flash it
1. Download the deauther `.bin` from this repo.
2. Download the flasher (`ESP8266Flasher.exe`) from this repo.
3. Plug the ESP8266 in over USB.
4. Open the flasher, click **Connect**, and pick the board's COM port (often COM5 or COM3).
5. In the **config** tab, select the deauther `.bin`.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/d2c45c98-a8a3-4943-b17a-da2601b63332" width="600" />
</p>

6. Go to the **operation** tab and click **Flash**. It takes about 2 to 5 minutes.
7. When it finishes, unplug and replug the board.

> **Tip:** the WiFi password for `pwned` is `deauther`, in case you were looking for it.

## Use it
Power the board from any USB source.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/20221cd2-76bf-434b-9c38-91b16dbfebd0" width="280" />
</p>

Connect to the board's WiFi network, then open `192.168.4.1` or `deauth.me` in a browser.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/185b65b9-ebe1-4352-ac5e-3d1374b60552" width="280" />
</p>

Accept the prompt.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/33cd1256-a1a9-4638-b908-0952eaed87fb" width="280" />
</p>

It auto-scans. Pick a network you own.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/0cb7426c-1336-44d2-9bf6-ff6e9f62867d" width="280" />
</p>

Open the attack menu (top left) and launch.

<p align="center">
<img src="https://github.com/Esther7171/ESP8266-Deauther/assets/122229257/393cb304-0098-41f8-821b-7ec9f9449e8f" width="280" />
</p>

## Reset
Flash the AI-Thinker reset file from the top of this repo, then flash the deauther firmware again.

## About
An IoT device for testing WiFi on an ESP8266. It is also a good project for learning WiFi, microcontrollers, Arduino, and both the offensive and defensive sides of wireless security.

## Disclaimer
This is a proof of concept for testing and education. The ESP8266 and its SDK were not built for this, so expect bugs. Use it only against your own networks and devices. Check the laws in your country first: deauthing or jamming networks you do not own is illegal in most places. I take no responsibility for misuse.

## Credits
Built on the open-source [ESP8266 Deauther](https://github.com/SpacehuhnTech/esp8266_deauther) by Spacehuhn Technologies.

Thanks for reading.
