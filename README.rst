==========================
ZenPacks.ZenSystems.ApcPdu
==========================


Description
===========

Provides support for APC PDU (Power Distribution Units) with component and performance  information for 
Power Supplies, Outlets and Banks.

This ZenPack is Zenoss 3 compliant.

Components
==========

    * The ZenPack has the following new Device Class

        * /Devices/Power/ApcPdu :
     
    * Components are:  
        * ApcPduPS   which has: 
            * Status details for power supplies
            * Performance graphs for power supply availability
        * ApcPduOutlet   which has: 
            * Status details for PDU outlets
            * Performance graphs for outlet load
        * ApcPduBank   which has: 
            * Status details for PDU banks
            * Performance graphs for bank load

    * Modeler plugins are:  
        * ApcPduDeviceMap   
            * Gathers Hardware and Software manufacturer and product
            * Serial number
        * ApcPduPSMap   
            * Gathers status information of power supplies
        * ApcPduOutletMap   
            * Gathers outlet name, number state and bank association
        * ApcPduBankMap   
            * Gathers bank number and state

There are no device-level templates for this device but each component detailed above, has component templates 
to generate performance graphs.

         

Requirements & Dependencies
===========================

    * Zenoss Versions Supported: 3.0
    * External Dependencies: The The APC PDU MIB needs to be available on target devices.
    * ZenPack Dependencies:
    * Installation Notes: zenhub and zopectl restart after installing this ZenPack.
    * Configuration: 

Download
========
Download the appropriate package for your Zenoss version from the list
below.

* Zenoss 3.0+ `Latest Package for Python 2.6`_

Installation
============
Normal Installation (packaged egg)
----------------------------------
Copy the downloaded .egg to your Zenoss server and run the following commands as the zenoss
user::

   zenpack --install <package.egg>
   zenhub restart
   zopectl restart

Developer Installation (link mode)
----------------------------------
If you wish to further develop and possibly contribute back to this 
ZenPack you should clone the git repository, then install the ZenPack in
developer mode::

   zenpack --link --install <package>
   zenhub restart
   zopectl restart

Configuration
=============

This ZenPack was tested with Zenoss 3.1 against APC AP 7952 B2 devices

Change History
==============
* 1.0
   * Initial Release
* 1.1
   * Some updates for extra debug
* 1.2
   * Transferred to new github methods

Screenshots
===========
|ApcPduComponents|


.. External References Below. Nothing Below This Line Should Be Rendered

.. _Latest Package for Python 2.6: https://github.com/jcurry/ZenPacks.ZenSystems.ApcPdu/blob/master/dist/ZenPacks.ZenSystems.ApcPdu-1.2-py2.6.egg?raw=true

.. |ApcPduComponents| image:: http://github.com/jcurry/ZenPacks.ZenSystems.ApcPdu/raw/master/screenshots/ApcPduComponents.jpg

                                                                        

