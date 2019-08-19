
<p style="color:red;font-weight:bold;font-size:5vw;"> disclaimer: this webpage is for personal testing purpose </p>
<br>
<br>
<h1>windows 10 initial setup keynotes</h1>

---last update 2019-07-30---

<div>
	
<p>---below is recommandation for reducing RAM and HDD usage.</p>

<h3>service: (disable all these)</h3>
<ul>
	<li>connected user experience</li>
	<li>sysmain/superfetch</li>
	<li>windows search</li>
	<li>windows update (also change recovery action to no action)</li>
	<li>HomeGroup Listener (1703 or earlier)</li> 
	<li>HomeGroup Provider (1703 or earlier)</li>
</ul>
<br>


<h3>c:\ </h3>
<ul>
	<li>-properties-tools-optimize-change settings- uncheck </li>
</ul>


<h3>task manager - startup:  </h3>
  <ul>
  <li>disable some apps </li>
</ul>

<h3>settings - update:  </h3>
  <ul>
  <li>advanced options: (depends)</li>
	<ul>
	<li>CHOOSE semi-anual/ current brunch for business (1809 or earlier)</li>
	<li>if needed, TURN ON pause updates (pause update once)</li>
	</ul>
</ul>
	
<h3>settings - update:</h3>
<ul>
  <li>delivery optim - TURN OFF allow downloads from other PCs.</li>
</ul>
	
<h3>settings - network:(optional)</h3>
<ul>
  <li>wifi - sel current wifi property - TURN ON meter connection</li>
</ul>

<h2>---belwo usually will be disable all on OOBE screen:</h2>
<ul>
	<li>setting - privacy - general TRUN OFF advertising ID</li>
	<li>setting - privacy - speech - TURN OFF Online Speech recognition </li> 
	<li>setting - privacy - inking & typing - TURN OFF </li>
	<li>setting - privacy - diagnostics - CHOOSE BASIC diagnostic data</li>
	<li>setting - privacy - diagnostics - TURN OFF tailored experiences</li>
	<li>setting - privacy - location - TURN OFF allow access to location</li>
	<li>setting - Update - Find my device - TURN OFF</li>
</ul>

<ul>
	<li>setting - privacy - app permissions:</li>
  	<ul>
	  <li>camera - choose apps</li>
	  <li>microphone - choose apps</li>
	  <li>voice activation - TURN OFF allow apps to use </li>
	</ul>

<li>settings - cortana:</li>
  <ul>
	<li>talk to cortana - lock screen - OFF</li>
	<li>permission - cloud search OFF; -history OFF & OFF</li>
  </ul>
  
<li>settings - cortana - more details - windows privacy options:</li>
  <ul>
	<li>general - ALL OFF</li>
	<li>speech - OFF (very important, sometimes OFF by default)  </li>
	<li>Inking & typing - OFF</li>
	<li>diagnstics - feedback freq - Never</li>
	<li>activity history - uncheck store my activity</li>
  </ul>	
  
<li>settings - personalization:
  <ul>
	  <li>colors - Transparency effects TURN OFF</li>
  </ul>

<li>microsoft store (or store) - settings:
  <ul>
	  <li>TURN OFF update option</li>
	</ul>
	
<li>vitual memory:
  <ul>
	  <li>for Surface 8G RAM + SSD: 512MB</li>
	  <li>for others 4G RAM + HDD: 1024 or 1536 MB</li>
	</ul>

</div>

<br>

<div>
---above changes will reduce the RAM and HDD usage. 
---highly recommand to make the changes.
---below are changes made to Win10, highly recommand:


hibernate/ fast startup: 
  (optional for HDD)
  if stratup time is too long, keep it ON.
  (recomand for SSD)
  DISABLE fast-startup, to reduce read/write.
  cmd>>> powercfg.exe -h off
  ctrl pnl - power option - power button do - ...

ctrl pnl - user account:
  change user acct ctrl settings - HIGH

right click taskbar:
  cortana - hidden

settings - account:
  sign-in options - privacy - OFF

settings - systems:
  tablet modes - sign in use desktop mode.

settings - device:
  bluetooth off (ON by default)
  typing - TURN ON show the touch keyboard when not in tablet mode.

settings - update: (Home edition)
  windows defender - TURN OFF device encryption

settings - apps - video playback:
  battery option - CHOOSE optm battery life
  Windows HD color settings - CHOOSE optm battery life
  and more...(depends)

regedit -
  disable adaptive contrast:(for sp4)
  regedit:
    HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Class\
    {4d36e968-e325-11ce-bfc1-08002be10318}\0001
    find FeatureTestControl, change from 9240 to 9250,
    save and restart to take effect

ctrl pnl - region and language: 
  administrative - change non-Unicode to Chinese
  restart system to take effect

ctrl pnl - power option:
  depends...
</div>

<div>

if no detail power option:
---below is to enable other power plans:
---do this will be disabling SLEEP mode, 
---do this will enable "Turn off Screen" button.

############################
###        Do Not        ### 
###  Press Power Button  ### 
###     Until disable    ###
### all sleep recall fn. ###
############################

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
  for details about different power modes, check another TXT file.
  (...depends)

NOTE: MAYBE every time change power plan, have to change following as well:
settings - display: 
  TURN OFF: change brightness automatically
settings - battery:
  TURN OFF: lower screen brightness in battery saver
</div>

<p>---end---</p>
