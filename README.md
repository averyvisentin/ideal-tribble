
## Run SPT-AKI server on separate machine


Hey all, today I'll be showing you how to run SPT-AKI server on a separate computer. Why would you do this? To save processing power for the game itself and increase performance. I mainly play SPT-AKI on my steam deck, and this was able to provide a significant performance increase. I'm using 3.8.3 version of SPT-AKI.




## You will need

- SPT-AKI server and client installed
- Flash drive (or FTP)
- 2 computers

## Installation

1. Locate your install of SPT-AKI (mine is "/home/games/escapefromtarkov/SPTAKI" yours will be different)

2. Plug in your flash drive and copy your entire SPT-AKI install to it (or use FTP)

3. Take that copy and place it wherever you desire on the server computer. Take note of it's location, we'll be editing some files in there.

4.  Open up the firewall manager on your computer. I'm hosting the server on Windows, so that will be Windows Defender Firewall (with advanced seccurity.
   ![mmc_k9jADgBRPY](https://github.com/averyvisentin/ideal-tribble/assets/88632224/c8b255c9-df8a-4717-9f23-692cfaaa0568)
Go to the Inbound rules on the left and click on new rule and select port, TCP and input the port number 6969.
![mmc_uQOQqQK0q8](https://github.com/averyvisentin/ideal-tribble/assets/88632224/5af8798f-d807-462a-91df-77b952697b4d)

Authorize the traffic on the next screen.

You will need to do this again for the UDP protocol on the Inbound Rules. Repeat those steps for the TCP and UDP Outbound rules as well.

6. Open you command prompt and type ipconfig, take note of your IPv4 address (mine is 192.168.1.15)
   ![WindowsTerminal_XKInALCfnc](https://github.com/averyvisentin/ideal-tribble/assets/88632224/3167d9d5-6d27-4b14-9975-084216a01303)


8. Naviagte to your SPT-AKI server install and edit 2 files

"~\Desktop\SPTAKI\Aki_Data\Server\database\server.json" and change the 127.0.0.1 to your local IPv4 address ex. 192.168.1.45, hit save
![notepad++_qJlfioUlnI](https://github.com/averyvisentin/ideal-tribble/assets/88632224/8f12e805-f0c9-4342-b8c2-bc0a6e0c454b)

"~\Desktop\SPTAKI\Aki_Data\Server\configs\http.json" and change both the ip and backendIp to your local IPv4 address ex. 192.168.1.45, hit save
![notepad++_co0C3gcqWg](https://github.com/averyvisentin/ideal-tribble/assets/88632224/b7f2b50c-7dff-4002-a0ec-e40b5eace2a2)


7. All done on the server PC, run the SPT-AKI server and head over to your PC you intend on playing with.

8. Launch the AKI-Launcher and head to the settings and change the 127.0.0.1 to your local IPv4 address ex. 192.168.1.45
  ![Aki Launcher_CnIlZe7wLH](https://github.com/averyvisentin/ideal-tribble/assets/88632224/7670b9a7-62ab-4d4b-9eb4-2169f839e191)



You can go a step further and port forward this in your router or you can use a VPN tunnel so your friends can play from wherever or you can access your server from whervever. It helps to assign a static IP address to your server PC otherwise you'll have to adjust to http:json or the server:json to whatever the router has decided your local IP to be.

Mods and everything work, you'll have to update them on both machines it might be possible to keep the folders synced using google drive or something similar, I just don't care to do it. (at the moment)
If you're playing on the steam deck, I'd recommend increasing your VRAM to 2GB in your BIOS, it helps to keep the frametimes stable.



Cheers!
