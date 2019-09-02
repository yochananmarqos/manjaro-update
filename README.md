# manjaro-update

This Bash script was initially made for myself, so it will make use of Pamac and Meld. Part of the code for the System Maintenance is from ```pacui``` https://github.com/excalibur1234/pacui

This script will also install Meld to your system in case it's not installed, for the simple reason because it will run a ```sudo pacdiff``` command and use Meld for the diff. 

So what is it actually doing?

  - Check for database lock file and remove it in case it's present
  - Remove partially downloaded packages
  - Mirrorsync and system update via Pacman
  - AUR update via installed AUR helper: yay, pikaur, aurman, pakku, trizen or pacaur
  - Search for orphaned packages and prompt for removal
  - Check for failed systemd service(s)
  - Check for broken symlinks
  - Check consistency of local repository
  - Check for packages moved to the AUR
  - Clean systemd log files
  - Clean package cache ( Note this will remove all package versions, except the latest 2 )
  - Check for EOL Kernels
  - Checks if Meld is installed and runs ```sudo pacdiff```
  - (If Installed) Updates Flatpaks and cleans via ```flatpak uninstall --unused```
  - (If Installed) Updates Snaps
  - (If Installed) Lists all installed Flatpaks and Snaps
  - Shows you how long it did take to run this script in seconds
