# uctronics-lcd-installer
This Repository has some bash Scripts in it that download and setup the neccessary Files for the UCtronics Rackmount LCD to show status Info.
The Installer creates a new Directory where this Repository and the UCTronics SKU_RM0004 Repository get downloaded into.

After downloading the necessary Files it will setup the I2C Interface and create a systemd Service to start the Status LCD
automagically at boot. (At the moment just Raspbian and RPI Kali Linux tested/ supported!)

The Installer also creates a backup of the /etc/modules and /boot/config.txt Files before changing them!

I'm not an expert Coder so use this Repo on your own Risk and don't blame me if you have to reinstall your Raspberry.

If you find something interesting within my Scripts feel free to copy parts of it and implement it into your own code.
Also feel free to contribute to this Repository and make it better :)


----------------------------------------------------------------
----------------------------------------------------------------
# INSTALLATION

    wget https://raw.githubusercontent.com/xXNightstalkerXx/uctronics-lcd-installer/master/uctronics-lcd-installer
Download the LCD-Installer Script with wget

    sudo chmod 0755 uctronics-lcd-installer
Make the file executable

    ./uctronics-lcd-installer
Launch the Installer Script
</br>
</br>
The Installer does the rest of the Job for you now.

----------------------------------------------------------------
----------------------------------------------------------------
# HOW TO USE

    sudo systemctl start uctronics-lcd
Will start the uctronics-lcd service and activate the Status LCD until reboot

    sudo systemctl stop uctronics-lcd
Will stop the uctronics-lcd service and deactivate the Status LCD

    sudo systemctl enable uctronics-lcd
Enables the automatic startup of the Status LCD after boot

    sudo systemctl disable uctronics-lcd
Disables the automatic startup of the Status LCD after boot

    uctronics-lcd-uninstaller
Will revert all changes to /etc/modules, /boot/config.txt and systemd and switch off the I2C Interface.
Also delete's all associated Files.
</br>
</br>
</br>
</br>
ATTENTION!!</br>
</br>
DO NOT install the UCTronics LCD Software with the UCTRONICS-LCD-AUTOINSTALLER and use the UCTRONICS-LCD-INSTALLER instead!!</br>
The UCTRONICS-LCD-AUTOINSTALLER is just meant to be used by my RPI-SETUP-TOOL!</br>
</br>

----------------------------------------------------------------
----------------------------------------------------------------
