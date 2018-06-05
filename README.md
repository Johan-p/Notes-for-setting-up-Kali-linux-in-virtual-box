Quick reference for kali linux setup guide in virtual box

# Download virtualbox from:
https://www.virtualbox.org/wiki/Downloads

Get both the installation as well as the Extension Pack.
Once virtual box is installed open the extention pack to add it to virtual box.

## Get the latest kali linux image for virtual box from:
https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-hyperv-image-download/

- Unzip the file.
- Create a new vm in virtual box and add the virtual disk.
- Now boot the VM.


# Installing the guest additions.
- In the Vbox menu add a shared drive (make sure to check auto-mount & make permament)
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

#### replace cdrom0 for the mounted media device if you run into any errors while copying.


- - -

## Setup

**NOTE**:
```bash
code
```


- - -
