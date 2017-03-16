# DeSmuMEaltWFC

Welcome to DeSmuME altWFC
=========================

The intention of this fork of DeSmuME is to have a more modern DeSmuME WiFi enabled version than the old DeSmuME 1.9.7 wifi recompiles that works better with the AltWFC server.

So in some ways we are aiming for an adapted DeSmuME 1.9.11 wifi or DeSmuME 1.9.12 wifi edition.


Dependencies and References
===========================

* DeSmuME 
	http://desmume.org
* AltWFC
	https://github.com/polaris-/dwc_network_server_emulator/wiki
	List of compatible NDS games: https://github.com/polaris-/dwc_network_server_emulator/wiki/Compatibility
	Tradeable pokemon in the GTS: http://pkmnclassic.net/gts/


Where to find the source and the newest executables
===================================================

The main branch of this fork is bound to a chosen reference version of DeSmuME, there will be side branches bound to the last regular DeSmuME release and current DeSmuME development efforts.

The source code and the executables are found at:
https://github.com/caela/DeSmuMEaltWFC.git



Contributions and acknowledgments
=================================

Contributions are highly welcome, as long as main functionality is not broken.
So far my thanks go to all of the DeSmuME team (full list further below), and there especially Luigi__ who was responsible for the WiFi breakthrough in the first place and to pleonex for sharing the source of his DeSmuME 1.9.7 wifi recompile.


How to use DeSmuME altWFC:
==========================

Currently we only have a working Windowsport.
Besides Windows, you'll need an ethernet connection and WinPCap installed. WinPCap comes with WireShark, so I recommend you install WireShark, so you additionally can monitor and document your network traffic.

If you don't have an ethernet connection an USB Tethered connection via your Android device will also work.

Before you start the executable for the first time:
* prepare your save file in the game so you would be allowed to enter the GTS
* patch your ROM, so you can connect with it to the AltWFC (details on their website), if AltWFC still doesn't speak https.

Start the executable for the first time as Administrator:
* Click on the general allowance and the firewall allowance
* Check the Wifi Settings: Choose 'Infrastructure' and your physical ethernet card in the drop down list
* Change any other settings you need to survive (Frame skip, controls...)
* Load the patched ROM until the subdirectory structure is created.
* You can stop DeSmuME altWFC and put your prepared save file (check that it still has the right name after the patching) in the Battery Folder.

DON'T USE YOUR OWN ARM7 and ARM9 BINARIES OR YOUR OWN FIRMWARE!!! (It would only decrease performance, anyway)

*Start DeSmuME altWFC as your normal user (WinPCap says its needs the application to be started as Admin once after every real Windowsrestart
*[This step can be skipped]. Now you can confirm that the Connection Test in the in games Wifi settings gives 'Connection Succesful'.
*Join the GTS in the game: Your MAC will be bound to your current DeSmuME instance, the immediate reconnect try will fail with 52200 ( I think the AltWFC actually has learned something wrong here...)
*Reload the ROM (don't restart DeSmuME!).
*[No longer necessary after latest changes: Go into the Nintendo Wifi settings and test connection, afterwards DON'T reload the ROM, but back out with B B B until the ROM restarts of itself.]
*Join the GTS again, this time it will work.
*As long as you don't close DeSmuME you can go into the GTS and restart your game as often as you want, it will always work (errors can happen but are seldom).

*If you close DeSmuMe, not just pause and hibernate it, next time you join the GTS you will have to renew your connection credentials again and basically do the same dance as the first time again. It's annnoying.


Specials and Troubleshooting:
=============================

*If you want to change from the default AltWFC server to another or your own AltWFC server, just change the DNS info in the games' internal Nintendo Wifi Settings. This info should then also be saved automatically in your desmume.ini settings file at the next NDS reload.

*If you encounter any of the quite seldom communication errors, it might help to go to the in games' Wifi Settings and test the connection from there (and ev. save the settings again). If you are extra kinky don't start the ROM again by reloading, but just by backing out of the settings until the ROM restarts of itself.

*Saving the settings in the in games' Wifi Settings will also allow you to see your Nintendo WFC Configuration again after a DeSmuME restart.

*If you are forced to erase your Nintendo WFC Configuration in the games options, don't confirm the firmware shutdown after erasing it, just reload the game again instead.

* Don't break the default ALTWFC server!!  If you want to contribute in the development and test some special things, it is recommended to setup your own AltWFC server first.


Liabilities:
============

As DeSmuME, this software comes WITHOUT ANY WARRANTY; without even the implied warranty of FITNESS FOR A PARTICULAR PURPOSE.
This software also falls under the same license as DeSmuME.



Caela, March 2017



****************
DeSmuME authors:
****************

Original author
---------------
yopyop

Current team
------------
Guillaume Duhamel
Normmatt
zeromus
rogerman

Contributors
------------
Bernat Muñoz (shash)
Allustar
amponzi
Anthony Molinaro
ape
Damien Nozay (damdoum)
delfare
Romain Vallet
snkmad
Theo Berkau
thoduv
Tim Seidel (Mighty Max)
Pascal Giard (evilynux)
Ben Jaques (masscat)
Jeff Bland
Bernat Muñoz (shash)
matusz
nitsuja
gocha
pa__
adelikat
hi-coder
WinterMute
pengvado
dormito
ldesnogue
mtheall
thelemonman
nash679
pokefan999
dottorleo
yki
Luigi__
CrazyMax
Riccardo Magliocchetti
CyberWarriorX
mic