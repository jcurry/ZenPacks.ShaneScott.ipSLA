=========================
ZenPacks.ShaneScott.ipSLA
=========================


Description
===========

This ZenPack gathers information about Cisco IP SLAs.  It has a modeler (SLA) that discovers such components
and several component templates that automatically bind to the SLA components to provide performance data.


Note that the component templates are NOT named identically to the component but specify within the SLAs.py code
that the component template for automatic binding, shall reflect rttMonCtrlAdminRttType.  In practise,
this means templates called Echo, HTTP, Jitter and New_SLA.

The SLAs component is created as a subclass of the existing OSComponent class.  No new device object class
is created and the __init__.py declares the relationship between the new SLAs component and the OperatingSystem
component.

A new device class, /Network/Cisco/IPSLA is created with modeler plugins assigned, including the SLA modeler.

Requirements & Dependencies
===========================

* Zenoss Versions Supported: 4.x - tested against Zenoss Core 4.2.5 SUP 457
* External Dependencies:
* ZenPack Dependencies:
* Installation Notes: Restart zenoss
  Note that you may get a message saying "Some unknown problem occured adding device class /Network/Cisco/IPSLA". This appears to be benign and the class is actually added.
* Configuration: none needed, put your device into /Network/Cisco/IPSLA, the modeler will discover the SLA instances as components and start graphing them.


Download
========
Download the appropriate package for your Zenoss version from the list
below.

* Zenoss 4.0+ `Latest Package for Python 2.7`_


Installation
============

Glitches have been seen during the installation process.  Attempting a second install is often successful.


Change History
==============
* 3.5.1
    * forked from Hackman238
* 3.5.2
    * Modifications made to services/SLAPerformanceConfig.py and zensla.py by Jane Curry
      to make data collection work
* 3.5.3
    * forked from jcurry
    * streamlined the code for github
* 3.5.4
    * Jane Curry - Changed order of methods in install in __init__.py
* 3.5.5
    * Charles Bueche - added MANIFEST.in to create a complete Zenpack, along with some debug code and a new screenshot.


===========
Screenshots
===========

See the screenshots directory


.. External References Below. Nothing Below This Line Should Be Rendered

.. _Latest Package for Python 2.7: https://github.com/jcurry/ZenPacks.ShaneScott.ipSLA/blob/master/dist/ZenPacks.ShaneScott.ipSLA-3.5.5-py2.7.egg?raw=true
