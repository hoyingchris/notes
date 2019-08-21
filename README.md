
**last update 20190821**

***for first time startup, do not connect to wifi.***

***recommend to run fresh start first to delete useless software.***

*below is recommendation for reducing RAM and HDD usage. *

**service: (disable all these)**
- connected user experience
- HomeGroup Listener (1703 or earlier) 
- HomeGroup Provider (1703 or earlier)
- sysmain/superfetch
- windows search
- windows update (also change recovery action to no action)

**c:\\ ** 

  -properties-tools-optimize-change settings- uncheck

task manager - startup:
-  disable some apps

settings - update:
-  advanced options: (depends)
   -	CHOOSE semi-anual/ current brunch for business (1809 or earlier)
	if needed, TURN ON pause updates (pause update once)

settings - update:
-  delivery optim - TURN OFF allow downloads from other PCs.

settings - network:(optional)
-  wifi - sel current wifi property - TURN ON meter connection
-  data usage - background connection OFF

settings - privacy - background
-  background apps - TURN OFF ALL

**belwo usually will be disable all on OOBE screen: **
- setting - privacy - general TRUN OFF advertising ID
- setting - privacy - speech - TURN OFF Online Speech recognition 
- setting - privacy - inking & typing - TURN OFF 
- setting - privacy - diagnostics - CHOOSE BASIC diagnostic data
- setting - privacy - diagnostics - TURN OFF tailored experiences
- setting - privacy - feedback - frequency - NEVER
- setting - privacy - location - TURN OFF allow access to location
- setting - Update - Find my device - TURN OFF

setting - privacy - app permissions:
-  camera - choose apps
-  microphone - choose apps
-  voice activation - TURN OFF allow apps to use 

settings - cortana:
 -  talk to cortana - lock screen - OFF
 -  permission - cloud search OFF; -history OFF & OFF

settings - cortana - more details - windows privacy options:
-  general - ALL OFF
-  speech - OFF (very important, sometimes OFF by default)
-  Inking & typing - OFF
-  diagnstics - feedback freq - Never
-  activity history - uncheck store my activity

settings - personalization:
-  colors - Transparency effects TURN OFF

microsoft store (or store) - settings:
-  TURN OFF update option

vitual memory:
-  for Surface 8G RAM + SSD: 512MB
-  for others 4G RAM + HDD: 1024 or 1536 MB


**above changes will reduce the RAM and HDD usage. ** 
**highly recommand to make the changes. **
**below are changes made to Win10, highly recommand: **


hibernate/ fast startup: 
-  (optional for HDD)
-  if stratup time is too long, keep it ON.
-  (recomand for SSD)
-  DISABLE fast-startup, to reduce read/write.
-  cmd>>> powercfg.exe -h off
-  ctrl pnl - power option - power button do - ...

ctrl pnl - user account:
-  change user acct ctrl settings - HIGH

right click taskbar:
-  cortana - hidden

settings - account:
-  sign-in options - privacy - OFF

settings - systems:
-  tablet modes - sign in use desktop mode.

settings - device:
-  bluetooth off (ON by default)
-  typing - TURN ON show the touch keyboard when not in tablet mode.

settings - update: (Home edition)
-  windows defender - TURN OFF device encryption

settings - apps - video playback:
-  battery option - CHOOSE optm battery life
-  Windows HD color settings - CHOOSE optm battery life
-  and more...(depends)

regedit -
-  disable adaptive contrast:(for sp4)
-  regedit:
   - HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Class\
    {4d36e968-e325-11ce-bfc1-08002be10318}\0001
-   find FeatureTestControl, change from 9240 to 9250,
-   save and restart to take effect

ctrl pnl - region and language: 
-  administrative - change non-Unicode to Chinese
-  restart system to take effect

ctrl pnl - power option:
-  depends...

**if no detail power option:**
**-below is to enable other power plans:**
**-do this will be disabling SLEEP mode, **
**-do this will enable "Turn off Screen" button.**

############################
***        Do Not        *** 
***  Press Power Button  *** 
***     Until disable    ***
*** all sleep recall fn. ***
############################

settings - systems:
-  power & sleep - Network Connection (WIFI) 
   - NEVER conncet to wifi while sleep.
   - which means: CHOOSE Always disconnect to wifi while sleep.
-  to check availabity of modern standby mode, go cmd
   - >>> powercfg /a
-  you can see "S0 Low Power Idle Network Connected" or "Disconnected".

cmd to check power mode detail options:
-  >>> poowercfg /q
- if want to make specific option to be appear again, look for correctsponding
- registry key and add DWON(32bit), name it "Attributes" and set value "2"

disable "modern standy":
- regedit:
  - HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power
  - under "CsEnabled", change the value from "1" to "0"
  - save and restart to take effect
  - after RESTART, detail power options will appear. 

ctrl pnl - power opt:
-   for details about different power modes, check another TXT file.
-   (...depends)

NOTE: MAYBE every time change power plan, have to change following as well:
settings - display: 
  TURN OFF: change brightness automatically
settings - battery:
  TURN OFF: lower screen brightness in battery saver

--end--
