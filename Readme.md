# Custom BSB-LAN Circuit Design Implementations

This repository contains custom hardware implementations for the [fredlcore/BSB-LAN](https://github.com/fredlcore/BSB-LAN/) interface. This repo is not offiliated with the original project.

Note: the designs are currently **untested**. This will be done in due course.


The PCBs have been laid out using Eagle PCB V6.6 and use predominantly surface mount components to make machine assembly easier. Parts used are all available for assembly in JLCPCBs parts catalogue.

A library file containing all parts used is included in the repository.

CAM files are included for generating 2-Layer and 4-Layer Gerber files using a naming scheme compatible with JLCs upload.

The repository contains a ULP file that can be run to generate the CPL/BOM files for upload to JLC. The `LCSC_PART` attribute has been added for each component to simplify generation of the assembly spreadsheets required by JLC. 


---

There are four hardware variants in this repository:

### BSB-LAN Daughter Board

Designed to work with the ESP32-POE-ISO controller or other Olimex boards with UEXT headers.

The PCB schematic is based on the design found at in the GitHub repository [fredlcore/BSB-LAN](https://github.com/fredlcore/BSB-LAN/), with some slight adaptions to provide ESD protection for the isolated B2B interface. 


### BSB-LAN PoE Ethernet DIN Mount (Single-Sided)

A full implementation including ESP32 controller, PoE Ethernet, USB programming and SD card interfaces. The single-sided version is designed for assembly using JLCs economic process.

The form factor of the board has been designed to fit in a Camdenboss CNMB/3/KIT DIN mount enclosure.


### BSB-LAN PoE Ethernet DIN Mount (Compact)

The same circuit and features as above, but using double-sided assembly to fit in a more compact Camdenboss CNMB/2/KIT DIN mount enclosure.

### BSB-LAN Wi-Fi DIN Mount

A full implementation including ESP32 controller, USB programming and SD card interfaces. This variant omits the LAN components to reduce the number of parts and make the board cheaper to manufacture. Power is supplied from either a 12V screw terminal (isolated through DC/DC for safety), or powered by the USB programming port.

Uses single-sided version is designed for assembly using JLCs economic process.

The form factor of the board has been designed to fit in a Camdenboss CNMB/2/KIT DIN mount enclosure.


---

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.  
