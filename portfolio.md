---
title: "GEODOS01B"
name: "AAA"
excerpt: "Open-source scintillation detector of ionizing radiation. The device can be further modified according to specific requirements. Character of its construction makes it especially suitable for placement into mountaints for in-field measurements"
header:
  image: products/GEODOS01B/doc/src/img/GEODOS_Chernobyl_redforest_site.jpg
  teaser: products/GEODOS01B/doc/src/img/GEODOS_Chernobyl_redforest_site.jpg
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: products/GEODOS01B/doc/src/img/GEODOS_Polednik_site.jpg

---


![GEODOS01A Installed on Polednik site](doc/src/img/GEODOS_Polednik_site.jpg)

### Locations

GEODOS devices are mounted on multiple significant locations around Europe at this moment.

#### Chernobyl Red Forest

One GEODOS device is installed in [Chernobyl Red Forest site](https://en.wikipedia.org/wiki/Red_Forest).

![GEODOS01A Installed in Chernobyl Red Forest site](doc/src/img/GEODOS_Chernobyl_redforest_site.jpg "GEODOS01A Installed in Chernobyl Red Forest site")

![GEODOS01A raw data before temperature compensation](doc/src/img/GEODOS_chernobyl_graph.png)

#### Šumava mountains

GEODOS devices are installed on multiple locations in Šumava. For example at [Polednik watch tower](https://cs.wikipedia.org/wiki/Poledn%C3%ADk_(%C5%A0umava)).

![GEODOS01A Installed on Polednik site](doc/src/img/GEODOS_Polednik_site.jpg)

### Technical parameters

* Detection element: scintillation crystal NaI(Tl), 10 mm in diameter, 20 mm in length; integrated with SiPM detector
* Power source: solar panel
* Backup power source: rechargable 18650 Li-ion cell
* Data memory: SD card
* Record’s content: energy and time of each event
* Record’s periodicity: 10 s (maximal dead time 2 s)
* Time resolution: 20 us
* ADC Conversion time: 104 us 
* [Dead time](https://en.wikipedia.org/wiki/Dead_time): 2 us
* Accuracy of event’s time: 500 ns
* Energy range: 0.3 to 1 MeV (0,2 MeV resolution)
* Open-source HW and SW
* Device status indicator type: LED
* Uniterrupted measurement interval: 365 days minimum
* LoRa connection to IoT network
* Weather resistivity IP 65


### Device block diagram

![GEODOS01A block diagram](hw/sch_pcb/GEODOS01B_block.png)

### Sensor element

The core of the detector is a scintillation crystal with [SiPM detector](https://en.wikipedia.org/wiki/Silicon_photomultiplier).

![Scintillation detector in box](doc/src/img/GEODOS01A_sensor.jpg)

![Scintillation detector housing](doc/src/img/GEODOS01A_sensor_box.jpg)

### Data storage

The primary raw data is stored in SDcard memory. The IoT network is used for telemetry data transfer, device monitoring (e.g. temperature, humidity, pressure, battery voltage etc.).  We are normally using the [TTN](https://www.thethingsnetwork.org/), but the device could be configured for use with any IoT LoRa based network.
For remote areas, mounting a IoT gateway in radio range of GEODOS instruments could be also a good option.

### Detailed documentation of used electronic modules

* [STEPUPDC02A](https://github.com/mlab-modules/STEPUPDC02)
* [AIRDOSC01A_PCB01C](https://github.com/UniversalScientificTechnologies/AIRDOSC01/tree/AIRDOSC01A/hw/sch_pcb/AIRDOSC01A_PCB01C)
* [PCRD06A](https://github.com/mlab-modules/PCRD06)
* [GPS01B](https://www.mlab.cz/module/GPS01B)
* [DATALOGGER01A](http://mlab.cz/module/DATALOGGER01A)
* [ALTIMET01A](https://github.com/mlab-modules/ALTIMET01)
* [ISM02B](https://github.com/mlab-modules/ISM02)
* [TPS63060V01A](https://github.com/mlab-modules/TPS63060V01)
* [LION1CELL01B](https://github.com/mlab-modules/LION1CELL01)
* [SOLARMINI01B](https://github.com/mlab-modules/SOLARMINI01)
