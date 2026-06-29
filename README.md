# ha-eink-wx
Home Assistant simple weather display for monochrome e-ink. Fits Seeedstudio XIAO 7.5" ePaper Panel ESP 800 x 480
<br>
inkwx.rtf is the contents of dashboard named inkwx. 
ha-display.yaml is my configuration based directly from the cookbook provided from Seeedstudio for use in Home Assistant.
<br>
<h1>Dependencies:</h1>
<br>  Wundergroundpws (Optional): weather underground plugin for personal weather stations
<br>  National Weather Service (NWS): national weather service for USA for forcast data
<br>  NWS Alerts: for pulling National Weather Service Alert/Watches/Warnings.
<br>  Ecowitt Official Integration (Optional): for Ecowitt weather stations or use your own PWS integration. If your PWS is fead into WUnderground, you can just use that.
<br>  Puppet: for generating png file of the created dashboard. 

<img src=eink_display_example.png>

<br>
<h1>Installation</h1>
Copy contents of <a href=inkwx.rtf>inkwx.rtf</a>. 
<br>
Create a new dashboard named inkwx. Edit the dashboard by clicking the pencil icon. Then click on the kabob menu (3 vertical dots) and select {}Raw Configuration Editor.
<br>
Paste contents of inkwx.rtf. 
<br>
Edit contents to have sensors match up with your personal Home Assistant setup. Change KSCFORTM52 to point to your personal weather station or a weather station local to you. The name should match the name in the Wundergroundpds configuration. Once all changes are configured, save changes.
<br>
The page should render through Puppet with this view:
<img src=dashboard-inkwx-puppet-output.png>
