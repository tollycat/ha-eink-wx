# ha-eink-wx
Home Assistant simple weather display for monochrome e-ink. Fits Seeedstudio XIAO 7.5" ePaper Panel ESP 800 x 480
<br><br>
The file named inkwx.rtf is the contents of dashboard named inkwx. 
<br><br>
The file named ha-display.yaml is my configuration based directly from the cookbook provided by Seeedstudio for use in Home Assistant.
<br>
<h1>Dependencies:</h1>
<ul>
  <li>Wundergroundpws (Optional): weather underground plugin for personal weather stations</li>
  <li>National Weather Service (NWS): national weather service for USA for forcast data</li>
  <li>NWS Alerts: for pulling National Weather Service Alert/Watches/Warnings.</li>
  <li>Ecowitt Official Integration (Optional): for Ecowitt weather stations or use your own PWS integration. If your PWS is fead into WUnderground, you can just use that.
  <li>Puppet: for generating png file of the created dashboard. </li>
</ul>
<br>
<img src="eink_display_example.png">

<br>
<h1>Installation</h1>
Copy contents of <a href="inkwx.rtf">inkwx.rtf</a>. 
<br><br>
Create a new dashboard named inkwx. Edit the dashboard by clicking the pencil icon. Then click on the kabob menu (3 vertical dots) and select {}Raw Configuration Editor.
<br><br>
Paste contents of inkwx.rtf. 
<br><br>
Edit contents to have sensors match up with your personal Home Assistant setup. Change KSCFORTM52 to point to your personal weather station or a weather station local to you. The name should match the name in the Wundergroundpds configuration. Once all changes are configured, save changes.
<br><br>
The page should render through Puppet with this view:
<img src=dashboard-inkwx-puppet-output.png>
<h2>Seeeedstudio provided instructions</h2>
The following section was provide by Seeedstudio on this <a href="https://wiki.seeedstudio.com/xiao_075inch_epaper_panel_esphome/" target="_blank">page.</a> The yaml provided on that page is what my <a href="ha-display.yaml"> ha-display.yaml </a> file.
<br><br>
On the Seeedstudio website follow Steps 1-3, then skip the "Basic usages" section.
Then proceed to the <a href="https://wiki.seeedstudio.com/xiao_075inch_epaper_panel_esphome/#demo-1-take-the-home-assistant-dashboard-as-a-screenshot" target="_blank"> "Take a screenshot" </a> section.
<br><br>
Now use the contents of the ha-display.yaml after the "captive_portal:" line and put into the yaml created when you added your device to ESPHome.
<h2>Customize</h2>
Now you need to change the puppet link to match your Home Assistant IP and the dashboard-{name}, replacing {name} with the name of your dashboard you are pulling for the e-ink display.
