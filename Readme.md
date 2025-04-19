# Boiler System Bus (BSB) Interface PCB Designs

This repository contains a series of PCB designs used to interface between the Boiler System Bus (BSB) of certain heating systems and network interfaces.

Note: the designs are currently **untested**. This will be done in due course.

## MCU Software

The hardware is compatible with the ESP32 software implementations from [fredlcore/BSB-LAN](https://github.com/fredlcore/BSB-LAN/). 
Note: This repo is **not affiliated** with said project in any way - support queries for these PCB designs should **not** be directed to that project.

## Hardware

The hardware is based around an ESP32 controller, with either PoE LAN or WiFi network connectivity.

The PCBs have been laid out using Eagle PCB V6.6 and use predominantly surface mount components to make machine assembly easier. Parts used are all available for assembly in JLCPCBs parts catalogue.

A library file containing all parts used is included in the repository.

CAM files are included for generating 2-Layer and 4-Layer Gerber files using a naming scheme compatible with JLCs upload.

The repository contains a ULP file that can be run to generate the CPL/BOM files for upload to JLC. 
The `LCSC_PART` and `JLC_X/Y/ROTATION` attributes have been added for each component to simplify generation of the assembly spreadsheets required by JLC. If changing the PCB designs, ensure these attributes are updated as necessary.

### BSB-to-UEXT Daughter Board

Designed to work with the ESP32-POE-ISO controller from Olimex, connecting vial the UEXT headers.

The PCB schematic is simply based on the design found at in the GitHub repository [fredlcore/BSB-LAN](https://github.com/fredlcore/BSB-LAN/tree/master/BSB_LAN/schematics).

There are some slight adaptions to provide ESD protection for the isolated B2B interface and designed to be surface-mount machine for machine assembly. 

### BSB-to-PoELaN for DIN Mount enclosure

A full implementation including ESP32 WROOM-32UE controller, PoE Ethernet power and networking, and USB programming and SD card interfaces.

The board and components have been designed for use with JLCPCBs economic assembly process. 

The form factor of the board has been designed to fit in a Camdenboss CNMB/3/KIT DIN mount enclosure to provide a tidy fully enclosed solution.

### BSB-to-WiFi for DIN Mount enclosure

A full implementation including ESP32 WROOM-32E controller, WiFi-only networking (PCB antenna, footprint compatible with external antenna), and USB programming and SD card interfaces.
This variant omits the LAN components to reduce the number of parts and make the board cheaper to manufacture. 
Power is supplied from either a 12V screw terminal (isolated through DC/DC for safety), or powered by the USB programming port.

The board and components have been designed for use with JLCPCBs economic assembly process. 

The form factor of the board has been designed to fit in a Camdenboss CNMB/2/KIT DIN mount enclosure to provide a tidy fully enclosed solution.


---

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.  
