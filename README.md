# MKS-PI-Clean-Klipper-Install
Unscrew the Klipper installation on the MKS-PI

Step 1: Righ now is a good time to download/ backup all your config files and any G-code files and macros you have.

Warning: All care is taken, no responsability accepted, if you FUBAR your install, you will have to reflash your drive, so refer back to step one.

Step 2: All this crap below :)

Log in via SSH, on windows, just use command propt, you dont need putty or anything else.

Once you have logged in, type the following commands:

sudo apt update

sudo apt upgrade

Wait for it to complete, then type:

cd ~

./kiauh/kiauh.sh

Now the Kiauh intoface will come up, and uninstall Fluid, Klipper and Moonraker.

Once they are all removed, then exit

Type the following:

cd ~

ls -a

That will show you a list of files and folders under the user folder, so much crap installed that shouldnt really be there, not needed, but its nice to see what crap Makerbase left on the image.

Anyway, deleate everything to do with Klipper:

sudo rm -r kiauh-backups

sudo rm -r kiauh

sudo rm -r klipper

sudo rm -r .kiauh.ini

sudo rm -r moonraker

sudo rm -r moonraker-env

sudo rm -r printer_data

sudo rm -r gcode_files

sudo reboot

log back into ssh after the MKS-PI reboots

then type:

cd ~

git clone https://github.com/th33xitus/kiauh.git

Once it completes. then type:

./kiauh/kiauh.sh

The Kiauh interface will load, and you can install klipper, then moonraker then Mainsail, note, due to this being and an un official OS it has an outdated version of Python, so when Kiauh asks, choose version 2.7.

Once all thats completed, you now hove an unfucked version of Klipper installed.

Upload you config files and you should be good to go

Regards

NexGen-3D
