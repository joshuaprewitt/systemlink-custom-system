By default, SystemLink uses the native operating system methods to get the vendor name, product/model name, and serial number information from the system (typically from the BIOS). In some cases you may want to customize how the system shows up in SystemLink especially if the PC/Controller is part of a larger "system".  In addition, in some cases vendors do not program this infomation into the BIOS when the device is manufactured and you may want to set it to make it easier to identify and track the PC/Controller as an asset.

# Customizing the System
You can change how a system shows up in the SystemLink systems grid and systems details by adding the following attributes to the C:\ProgramData\National Instruments\salt\conf\grains text file on Windows or /etc/salt/grains text file on NI Linux RT. You may need to restart your client for the changes to take effect.

manufacturer: Vendor 123
productname: Model ABC
serialnumber: 123456

# Customizing the PC/Controller Asset
You can modify how the PC/controller for you system shows up in the asset manager by modifing the registry keys in the [pc asset](pc%20asset) folder with a text editor. Next, import the registry keys on the client, which you can easily do by double-clicking on them.  This will change how the PC shows up in the SystemLink Asset Manager as well as MAX and NXG.  You may need to restart your client for the changes to take effect and it may result in a duplicate asset for the controller with the new information if the client was already connected to a server.  If this happens you can delete the old asset.
