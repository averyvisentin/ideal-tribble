
## Run SPT-AKI server on separate machine


Hey all, today I'll be teaching you how to run SPT-AKI server on a separate computer. Why would you do this? To save processing power for the game itself and increase performance. I mainly play SPT-AKI on my steam deck, and this was able to provide a significant performance increase. I'm using 3.8.3 version of SPT-AKI.




## You will need

- SPT-AKI server and client installed
- Flash drive (or FTP)
- 2 computers

## Installation

1. Locate your install of SPT-AKI (mine is "/home/games/escapefromtarkov/SPTAKI" yours will be different)

2. Plug in your flash drive and copy your entire SPT-AKI install to it (or use FTP)

3. Take that copy and place it wherever you desire on the server computer. Take note of it's location, we'll be editing some files in there.

4.  Open up the firewall manager on your computer. I'm hosting the server on Windows, so that will be Windows Defender Firewall. Go to the Inbound rulles on the left and click on new rule and select port, TCP and input the port number 6969. Authorize the traffic on the next screen. 
You will need to do this again for the UDP protocol on the Inbound Rules. Repeat those steps for the TCP and UDP Outbound rules as well.

5. Open you command prompt and type ipconfig, take note of your IPv4 address (mine is 192.168.1.15)

6. Naviagte to your SPT-AKI server install and edit 2 files

"~\Desktop\SPTAKI\Aki_Data\Server\database\server.json" and change the 127.0.0.1 to your local IPv4 address ex. 192.168.1.15, hit save

"~\Desktop\SPTAKI\Aki_Data\Server\configs\http.json" and change both the ip and backendIp to your local IPv4 address ex. 192.168.1.15, hit save

7. All done on the server PC, run the SPT-AKI server and head over to your PC you intend on playing with.

8. Launch the AKI-Launcher and head to the settings and change the 127.0.0.1 to your local IPv4 address ex. 192.168.1.15


You can go a step further and port forward this in your router so your friends can play from wherever or you can access your server from whervever. It helps to assign a static IP address to your server PC otherwise you'll have to adjust to http:json or the server:json to whatever the router has decided your local IP to be.

Mods and everything work, you'll have to update them on both machines it might be possible to keep the folders synced using google drive or something similar, I just don't care to do it.
