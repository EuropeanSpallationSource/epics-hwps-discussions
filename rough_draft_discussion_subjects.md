#Hardware platform support


* When 15:45 - 17:45
* Room: Medicom Village Auditorium, ESS
* Subject : Discussion about support of different hardware platforms (RPi, MTCA, design sharing, open source solutions,FPGA...) in EPICS

My first question to myself is *What is hardware?*, then I searched them in EPICS site, and found the page which has the name of *Hardware Support: by Bus, by Manufacturer, by Contact Name, or By Link* at http://www.aps.anl.gov/epics/modules/bus.php

And I sent an email to Teck-talk at http://www.aps.anl.gov/epics/tech-talk/2016/msg00908.php, but no one actually reply yet! Anyway, better than nothing, so I did small preparations for this meeting. I think, most of HW can talk by using ASYN already. 

## RPi or others?

Tech-talk Search Results : Found 124 pages for "raspberry pi" (most recent first)

* GPIO   : https://github.com/ffeldbauer/epics-devgpio
* I2C    : https://github.com/ffeldbauer/drvAsynI2C
* Serial : https://github.com/jeonghanlee/gconpi

## Crate or Chasis, or Power Distribution Units, or pizza-box Management
  * monitor/change a status of HW though EPICS
  * update/revert the corresponding firmware through EPICS

###  SNMP (FRIB), we can use it for Wiener Products (e.g., Wiener VME Crate), and APC Power Distribution Unit

* https://groups.nscl.msu.edu/controls/ FRIB internal, Download source file
* https://github.com/EuropeanSpallationSource/snmp-nscl A forked the latest FRIB sources by ESS

Note that the Wiener is developing SNMPV3 support currently. We can use this for the most SNMP supported Network devices (Printers, Network Switches, Power Distribution Unit, Servers, and so on)

### IPMI (SLAC), we can use it for IPMI-based systems (e.g., xTCA systems)

* SLAC internal


## Common Industrial Protocol and others
* EtherNetIP (Siemens) -  EtherIP,   https://github.com/EPICSTools/ether_ip
* EtherCAT (Beckhoff)
- EtherCAT, http://controls.diamond.ac.uk/downloads/support/ethercat/
- Anders SANDSTRÖM, Motion Control with Open Source EtherCAT
* DeviceNet - fews in Tech-talks, but ...
* CompoNet - No files matched your search.
* ControlNet -??
* Siemens (ProfitNet)
-  S7Plc, http://epics.web.psi.ch/style/software/s7plc/s7plc.html
- ASYN based S7 PLC driver (Tomorrow talk) 
* Modbus - https://github.com/epics-modules/modbus
	
	

## xTCA

* 10th meeting of the xTCA interest group https://indico.cern.ch/event/470196/

* Open Source Firmware for MMC controller https://github.com/lnls-dig/openMMC
* the xTCA evaluation project in PH-ESE https://twiki.cern.ch/twiki/bin/view/XTCA/PHESExTCAEvaluationProject
* MTCA OPEN HW http://www.ohwr.org/projects
Beam Diagnostics group of the Brazilian Synchrotron Light Laboratory - LNLS https://github.com/lnls-dig
** AMC FMC Carrier (AFC) http://www.ohwr.org/projects/afc/wiki
** AMC FMC Carrier Kintex (AFCK) http://www.ohwr.org/projects/afck/wiki
** FMC ADC 130M 16B 4CHA http://www.ohwr.org/projects/fmc-adc-130m-16b-4cha/wiki
** Beam Positoning Monitor - RF Front-End http://www.ohwr.org/projects/bpm-rffe/wiki

* Anything else within EPICS community?


## VME
* MVME 3xxx / 5100 / 6100 (VxWorks, RTEMS)
* IOxOS IF 1210/1211 (EDLK)
* Struck SIS3316 digitizer
* OMS MAXv motor controller
* Highland V375 arbitrary waveform generator
* IP-carrier with boards for digital io

## Memory mapped register devices (FPGA) / HPS Common Platform Software
* PSI, *RegDev: A generic and flexible device support for memory mapped register devices*  https://github.com/paulscherrerinstitute/regdev
* SLAC, A Common Platform Software (CPSW) framework, LCLS-2 status talk. 

## Related Talks ? tomorrow 

* RegDev: A generic and flexible device support for memory mapped register devices
* ASYN based S7 PLC driver
* Introduction of device support for VMIVME-5565 and its usage at KEK
* DEVELOPMENT OF ADVANCED DATA AND IMAGE ACQUISITION SYSTEMS USING RIO TECHNOLOGY AND EPICS: INTEGRATION IN ITER
* Motion Control with Open Source EtherCAT
