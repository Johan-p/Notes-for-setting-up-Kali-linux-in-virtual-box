Quick reference for kali linux setup guide in virtual box

# Download virtualbox from:
[virtual box](https://www.virtualbox.org/wiki/Downloads)

Get both the installation as well as the Extension Pack.

While we wait for the virtual box download lets download the kali .ova from the offensive-security site.

[Virtual box Kali Images](https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-hyperv-image-download/)

Be sure to select virtual box image before downloading.

Now install virtual box, and add the extension pack by dubbleclicking it.

Once our Kali image is downloaded import it.

In the menu go to file import appliance.

![import image](https://github.com/MarvinTheParanoidPentester/KalivboxSetupguide/blob/master/import.jpg?raw=true)

Check the Reinitilize the MAC address of all network cards and select import.

This might take a while...

#### Optional
On the network tab.
- Change the network adapters, set the first one to internal if you run a testing lab.
- Add a second adapter and set it to either NAT or bridged (bridged if you want to be able to attack any routers in the outside network)

On USB tab.
- Add any usb drivers you wish to add (for example a wireless usb adapter)

- Note if you have trouble mounting usb devices on windows 10 in virtual box; try changing the following setting in your registry editor.
  - open registry editor run > regedit
  - browse to HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Class{36fc9e60-c465-11cf-8056- 444553540000}
  - Delete the key named upper filters
  - restart your windows pc
  - this should fix any usb mounting issue's with virtual box on windows 10

On the Shared folders tab
- Add a shared drive (make sure to check auto-mount & make permament)
- optional you can set it to read-only, if you don't want kali to be able to write your machine.



#### Installing the guest additions & adding a shared drive.
- 
- Insert the guest additions cd from the virtual box devices menu.
- wait a moment for kali to pickup the new media (it should appear on your desktop)
  - you can ignore any auto-run as it won't work.

### Run the following in commandline to install the guest additions.
```bash
cp /media/cdrom0/VBoxLinuxAdditions.run /root/
chmod 755 /root/VBoxLinuxAdditions.run
cd ~/
./VBoxLinuxAdditions.run
reboot
```
Replace cdrom0 for the mounted media device if you run into any errors while copying.

- - -

## Setup

**NOTE**:
```bash
code
```

- - -
