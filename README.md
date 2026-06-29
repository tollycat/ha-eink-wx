# ha-eink-wx
Home Assistant simple weather display for monochrome e-ink. Fits Seeedstudio XIAO 7.5" ePaper Panel ESP 800 x 480
inkwx.rtf is the contents of dashboard named inkwx. 
ha-display.yaml is my configuration based directly from the cookbook provided from Seeedstudio for use in Home Assistant.
Dependencies: weather underground pws plugin; Wundergroundpws
  Wundergroundpws (Optional): weather underground plugin for personal weather stations
  National Weather Service (NWS): national weather service for USA for forcast data
  NWS Alerts: for pulling National Weather Service Alert/Watches/Warnings.
  Ecowitt Official Integration (Optional): for Ecowitt weather stations or use your own PWS integration. If your PWS is fead into WUnderground, you can just use that.
