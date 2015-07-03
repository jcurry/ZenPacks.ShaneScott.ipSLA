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
is created and the __init__.py decalres the relationship between the new SLAs component and the OperatingSystem
component.

A new device class, /Network/Cisco/IPSLA is created whith modeler plugins assigned, including the SLA modeler.


Change History
==============
* 3.5.1
    * forked from Hackman238
* 3.5.2
    * Modifications made to services/SLAPerformanceConfig.py and zensla.py by Jane Curry
      to make data collection work

===========
Screenshots
===========

See the screenshots directory




