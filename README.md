
---last update 20190822---
<br>
<p><b>for first time startup, do not connect to wifi.</b></p>
<hr>
<h2>
Stage 1
fast tune up for reducing RAM and HDD usage:
</h2>
<pre>
task manager - startup:
  disable some apps

service: (disable all these)
  connected user experience
  HomeGroup Listener (1703 or earlier) 
  HomeGroup Provider (1703 or earlier)
  sysmain/superfetch
  windows search
  windows update (also change recovery action to no action)

c:\ 
  -properties-tools-optimize-change settings- uncheck

settings - privacy - background
  background apps - TURN OFF ALL

...now can turn on WIFI...
...and do quickly for the following 3 steps...

microsoft store (or store) - settings: (need wifi connection)
  TURN OFF auto update option

settings - network:(optional)
  wifi - select current wifi property - TURN ON meter connection
  data usage - background data - ALWAYS RESTRICT

</pre>
<h2>
Stage 2
advance tune up:
</h2>
<pre>
below usually have be disabled on OOBE screen:
 setting - privacy - general TRUN OFF advertising ID
 setting - privacy - speech - TURN OFF Online Speech recognition 
 setting - privacy - inking & typing - TURN OFF 
 setting - privacy - diagnostics - CHOOSE BASIC diagnostic data
 setting - privacy - diagnostics - TURN OFF tailored experiences
 setting - privacy - location - TURN OFF allow access to location
 setting - Update - Find my device - TURN OFF

settings - Privacy:
  general - ALL OFF
  speech - OFF (very important)
  Inking & typing - OFF
  diagnstics - feedback freq - Never
  activity history - uncheck store my activity
  voice activation - TURN OFF allow apps to use 
  background apps - OFF
  
settings - update - update:
  change active hours:
	(depends...)
  advanced options: 
	(depends...)
	CHOOSE semi-anual/ current brunch for business (1809 or earlier)
	or TURN ON pause updates (pause update once)
	or CHOOse update MS product

settings - update:
  delivery optim - TURN OFF allow downloads from other PCs.

settings - cortana:
  talk to cortana - lock screen - OFF

vitual memory:
  for Surface 8G RAM + SSD: 512MB
  for others 4G RAM + HDD: 1024 or 1536 MB
</pre>

<h2>
Stage 3
customization:
</h2>
<pre>
setting - system:
  Display 	- OFF auto brightness
  Power&Sleep 	- ALWAYS disconnect from the network when sleep
  Battery 	- OFF lower screen brightness 

settings - device:
  bluetooth 	- OFF (ON by default)
  typing 	- TURN ON show the touch keyboard when not in tablet mode.

settings - personalization:
  colors - TURN OFF Transparency effects
  Taskbar - WHEN FULL combine taskbar button

settings - Apps
  offline maps - OFF auto update maps
  video playback - CHOOSE prefer to play at lower resolution
  		 - CHOOSE optm battery life
  		 - Windows HD color settings - CHOOSE optm battery life
  
settings - account:
  sign-in options - privacy - OFF

settings - Time&Language
  Language - Add Language

settings - search
  Permission - OFF cloud search
             - OFF History

setting - privacy - app permissions:
  review each options (depends...)  
  Account Info - Change Button (at the top) - OFF
  Contacts - Change Button - OFF

settings: (depends...)
  (1803 or later)
  update - windows defender - TURN OFF device encryption
  (before 1803)
  system - about - TURN OFF device encryption
  
ctrl pnl - user account:
  change user acct ctrl settings - HIGH

ctrl pnl - region and language: 
  administrative - change non-Unicode to Chinese
  (restart required)

ctrl pnl - power option: (depends...)
  hibernate/ fast startup: 
  (optional for HDD)
    if stratup time is too long, keep it ON.
  (recomand for SSD)
    DISABLE fast-startup, to reduce read/write.
      - cmd: powercfg.exe -h off
      - ctrl pnl - power option - power button do - ...

regedit - disable adaptive contrast:(for sp4)
  regedit:
    HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Class\
    {4d36e968-e325-11ce-bfc1-08002be10318}\0001
  find FeatureTestControl, change from 9240 to 9250,
  save and restart to take effect
</pre>

<h2>
Extra Stage:
</h2>
<pre>
if no detail power option:
  below is to enable other power plans:
  do this will be disabling SLEEP mode, 
  do this will enable "Turn off Screen" button.

DO NOT
PRESS POWER BUTTON
UNTIL DISABLE
ALL SLEEP RECALL FN.

settings - systems:
  power & sleep - Network Connection (WIFI) 
  - NEVER conncet to wifi while sleep.
  - which means: CHOOSE Always disconnect to wifi while sleep.
  to check availabity of modern standby mode, go cmd
  >>> powercfg /a
  you can see "S0 Low Power Idle Network Connected" or "Disconnected".

cmd to check power mode detail options:
  >>> poowercfg /q
if want to make specific option to be appear again, look for correctsponding
registry key and add DWON(32bit), name it "Attributes" and set value "2"

disable "modern standy":
regedit:
  HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power
  under "CsEnabled", change the value from "1" to "0"
  save and restart to take effect
  after RESTART, detail power options will appear. 

ctrl pnl - power opt:
  (...depends)

NOTE: MAYBE every time change power plan, have to change following as well:
settings - system - display: 
  TURN OFF: change brightness automatically
settings - system - battery:
  TURN OFF: lower screen brightness in battery saver
</pre>
<hr>
<p><em>---end---</em></p>
