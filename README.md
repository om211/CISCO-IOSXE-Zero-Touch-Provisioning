# CISCO-IOSXE-Zero-Touch-Provisioning
ZTP(Zero-Touch Provisioning) automates the process of installing or upgrading software images,
and installing configuration files on Cisco catalyst switches that are deployed first time in the network.
It reduces manual tasks such as upgrading and configuring the devices.
When a device that supports Zero-Touch Provisioning boots up, and does not find the startup configuration
(during fresh install on Day Zero), the device enters the Zero-Touch Provisioning mode.
The device locates a Dynamic Host Configuration Protocol (DHCP) server, bootstraps itself with its interface IP address, gateway, and Domain Name System (DNS) server IP address, and enables Guestshell. 
The device then obtains the IP address or URL of a TFTP or HTTP server, and downloads a Python script to configure the device. 
Guestshell provides the environment for the Python script to run. Using this model, you can roll out hundreds of switches with fully customizable and without any error prone manual configuration process.

Incase if DHCP server is configured for PnP process, after receiving DHCP response the PnP agent process that is running on a Cisco IOS-XE device is initiated.
In the absence of the startup configuration it attempts to connect the PnP server and the PnP process is continued. In case Zero-Touch Provisioning and PnP fails,
the device falls back to auto install to load configuration files. 
