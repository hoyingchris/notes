<style>
#subtitle {
	font-weight:bold;
	
}
#subcomment {
	font-weight:bold;
	font-style:italic;
}
li {
list-style-type:none;
}

</style>
<p style="color:red;font-weight:bold;font-size:5vw;"> disclaimer: this webpage is for personal testing purpose </p>
<br>
<br>
<h1>windows 10 initial setup keynotes</h1>

---last update 2019-07-30---

<div>
	
<p id="subcomment">---below is recommandation for reducing RAM and HDD usage.</p>

<p id="subtitle">service: (disable all these)</p>
<ul>
	<li>connected user experience</li>
	<li>sysmain/superfetch</li>
	<li>windows search</li>
	<li>windows update (also change recovery action to no action)</li>
	<li>HomeGroup Listener (1703 or earlier)</li> 
	<li>HomeGroup Provider (1703 or earlier)</li>
</ul>
<br>


<p id="subtitle">c:\ </p>
<ul>
	<li>-properties-tools-optimize-change settings- uncheck </li>
</ul>


<p id="subtitle">task manager - startup:  </p>
  <ul>
  <li>disable some apps </li>
</ul>

<p id="subtitle">settings - update:  </p>
  <ul>
  <li>advanced options: (depends)</li>
	<ul>
	<li>CHOOSE semi-anual/ current brunch for business (1809 or earlier)</li>
	<li>if needed, TURN ON pause updates (pause update once)</li>
	</ul>
</ul>
	
<p id="subtitle">settings - update:</p>
<ul>
  <li>delivery optim - TURN OFF allow downloads from other PCs.</li>
</ul>
	
<p id="subtitle">settings - network:(optional)</p>
<ul>
  <li>wifi - sel current wifi property - TURN ON meter connection</li>
</ul>

<p id="subcomment">---belwo usually will be disable all on OOBE screen:</p>
<ul>
	<li>setting - privacy - general TRUN OFF advertising ID</li>
	<li>setting - privacy - speech - TURN OFF Online Speech recognition </li> 
	<li>setting - privacy - inking & typing - TURN OFF </li>
	<li>setting - privacy - diagnostics - CHOOSE BASIC diagnostic data</li>
	<li>setting - privacy - diagnostics - TURN OFF tailored experiences</li>
	<li>setting - privacy - location - TURN OFF allow access to location</li>
	<li>setting - Update - Find my device - TURN OFF</li>
</ul>


<p id="subtitle">setting - privacy - app permissions:</p>
  	<ul>
	  <li>camera - choose apps</li>
	  <li>microphone - choose apps</li>
	  <li>voice activation - TURN OFF allow apps to use </li>
	</ul>

<p id="subtitle">settings - cortana:</p>
  <ul>
	<li>talk to cortana - lock screen - OFF</li>
	<li>permission - cloud search OFF; -history OFF & OFF</li>
  </ul>
  
<p id="subtitle">settings - cortana - more details - windows privacy options:</p>
  <ul>
	<li>general - ALL OFF</li>
	<li>speech - OFF (very important, sometimes OFF by default)  </li>
	<li>Inking & typing - OFF</li>
	<li>diagnstics - feedback freq - Never</li>
	<li>activity history - uncheck store my activity</li>
  </ul>	
  
<p id="subtitle">settings - personalization: </p>
  <ul>
	  <li>colors - Transparency effects TURN OFF</li>
  </ul>

<p id="subtitle">microsoft store (or store) - settings: </p>
  <ul>
	  <li>TURN OFF update option</li>
	</ul>
	
<p id="subtitle">vitual memory: </p>
  <ul>
	  <li>for Surface 8G RAM + SSD: 512MB</li>
	  <li>for others 4G RAM + HDD: 1024 or 1536 MB</li>
	</ul>

</div>

<br>

<div>
	<p id="subcomment">---above changes will reduce the RAM and HDD usage. </p>
	<p id="subcomment">---highly recommand to make the changes.</p>
	<p id="subcomment">---below are changes made to Win10, highly recommand:</p>

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
hello world </div>


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
