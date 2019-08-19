
<p style="color:red;font-weight:bold;font-size:5vw;"> disclaimer: this webpage is for personal testing purpose </p>
<br>
<br>
<h1>windows 10 initial setup keynotes</h1>

---last update 2019-07-30---

<div>
	
<h3>---below is recommandation for reducing RAM and HDD usage.</h2>

<p>service: (disable all these)</p>
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

<h3>---belwo usually will be disable all on OOBE screen:</h3>
<ul>
	<li>setting - privacy - general TRUN OFF advertising ID</li>
	<li>setting - privacy - speech - TURN OFF Online Speech recognition </li> 
	<li>setting - privacy - inking & typing - TURN OFF </li>
	<li>setting - privacy - diagnostics - CHOOSE BASIC diagnostic data</li>
	<li>setting - privacy - diagnostics - TURN OFF tailored experiences</li>
	<li>setting - privacy - location - TURN OFF allow access to location</li>
	<li>setting - Update - Find my device - TURN OFF</li>
</ul>


<h3>setting - privacy - app permissions:</h3>
  	<ul>
	  <li>camera - choose apps</li>
	  <li>microphone - choose apps</li>
	  <li>voice activation - TURN OFF allow apps to use </li>
	</ul>

<h3>settings - cortana:</h3>
  <ul>
	<li>talk to cortana - lock screen - OFF</li>
	<li>permission - cloud search OFF; -history OFF & OFF</li>
  </ul>
  
<h3>settings - cortana - more details - windows privacy options:</h3>
  <ul>
	<li>general - ALL OFF</li>
	<li>speech - OFF (very important, sometimes OFF by default)  </li>
	<li>Inking & typing - OFF</li>
	<li>diagnstics - feedback freq - Never</li>
	<li>activity history - uncheck store my activity</li>
  </ul>	
  
<h3>settings - personalization: </h3>
  <ul>
	  <li>colors - Transparency effects TURN OFF</li>
  </ul>

<h3>microsoft store (or store) - settings: </h3>
  <ul>
	  <li>TURN OFF update option</li>
	</ul>
	
<h3>vitual memory: </h3>
  <ul>
	  <li>for Surface 8G RAM + SSD: 512MB</li>
	  <li>for others 4G RAM + HDD: 1024 or 1536 MB</li>
	</ul>

</div>

<br>

<div>
	<p>---above changes will reduce the RAM and HDD usage. </p>
	<p>---highly recommand to make the changes.</p>
	<p>---below are changes made to Win10, highly recommand:</p>

<dl>
	<dt>hibernate/ fast startup: </dt>
	<dd>(optional for HDD) </dd>
	<dd>if stratup time is too long, keep it ON. </dd>
	<dd>(recomand for SSD) </dd>
	<dt>DISABLE fast-startup, to reduce read/write. </dt>
	<dd>cmd>>> powercfg.exe -h off </dd>
	<dd>ctrl pnl - power option - power button do - ... </dd>
</dl>
<dl>
<dt>ctrl pnl - user account:</dt>
 <dd>change user acct ctrl settings - HIGH </dd>
 </dl>

<dl>
	<dt>right click taskbar: <dt>
	<dd>cortana - hidden</dd>
</dl>
	
<dl>
	<dt>settings - account: </dt>
	<dd>sign-in options - privacy - OFF </dd>
</dl>

<dl>
	<dt>settings - systems: </dt>
	<dd> tablet modes - sign in use desktop mode. </dd>
</dl>
<dl>
<dt>settings - device: </dt>
<dd>  bluetooth off (ON by default) </dd>
<dd>  typing - TURN ON show the touch keyboard when not in tablet mode. </dd>
</dl>
<dl>
	<dt>settings - update: (Home edition)</dt>
	<dd>  windows defender - TURN OFF device encryption </dd>
</dl>
<dl>
	<dt>settings - apps - video playback: </dt>
	<dd>  battery option - CHOOSE optm battery life </dd>
	<dd>  Windows HD color settings - CHOOSE optm battery life </dd>
	<dd>  and more...(depends) </dd>
</dl>
<dl>
<dt>regedit - <dt>
<dd>  disable adaptive contrast:(for sp4) </dt>
<dl>
	<dt>regedit: </dt>
    <dd>
    HKEY_LOCAL_MACHINE\SYSTEM\ControlSet001\Control\Class\
    {4d36e968-e325-11ce-bfc1-08002be10318}\0001
    </dd>
    <dd>find FeatureTestControl, <br> change from 9240 to 9250,<br>
	    save and restart to take effect</dd>
</dl>

<dl>
<dt>ctrl pnl - region and language: </dt>
<dd>  administrative - change non-Unicode to Chinese </dd>
<dd>  restart system to take effect </dd>
</dl>

<dl>
	<dt>ctrl pnl - power option: </dt>
	<dd>  depends... </dd>
</dl>
<p></p>
</div>


<div>
<pre>
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
</pre>
</div>

<p>---end---</p>
