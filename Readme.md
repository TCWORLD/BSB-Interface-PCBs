BSB-LAN Circuit Design for ESP32-POE-ISO
----

This repository contains a hardware implementation for the BSB-LAN interface designed to work with the ESP32-POE-ISO controller board.

The PCB schematic is based on the design found at in the GitHub repository [fredlcore/BSB-LAN](https://github.com/fredlcore/BSB-LAN/), with some slight adaptions to provide ESD protection for the isolated B2B interface. 

The PCB has been laid out using Eagle PCB V6.6. It uses predominantly surface mount components to make machine assembly easier. Parts used are all available for assembly in JLCPCBs parts catalogue. The `LCSC_PART` attribute has been added for each component to simplify generation of the assembly spreadsheets required by JLC.


---

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.  
