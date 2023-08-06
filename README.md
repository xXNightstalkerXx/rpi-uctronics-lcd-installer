# uctronics-lcd-installer
This Repository has some bash Scripts in it that download and setup the neccessary Files for the UCtronics Rackmount LCD to show status Info.
The Installer creates a new Directory where this Repository and the UCTronics SKU_RM0004 Repository get downloaded into.

After downloading the necessary Files it will setup the I2C Interface, and depending on the OS, setup a custom Startup Script
which will launch the LCD Status Display at every boot. (At the moment just Raspbian and RPI Kali Linux supported!)

On Raspbian it will launch the Startup Script with the rc.local file.
On Kali Linux it has to insert a Cron job to start the Script because there is no rc.local file.

The Installer also creates a backup of these Files before changing them!

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

    uctronics-lcd-startup
Will manually activate the Startup Script and launch the Status LCD Display

    uctronics-lcd-uninstaller
Will revert all changes to rc.local and config.txt file and switch off I2C Interface.
Also delete's all associated Files.

----------------------------------------------------------------
----------------------------------------------------------------
