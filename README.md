# Total Annihilation Linux Wine

How to get Total Annihilation running on Linux with IPX wrapper for LAN games

## Installation

First, download [Lutis](https://lutris.net/downloads), this is a game manger for linux and comes with runners for windows games.

Next, log in to your GOG account and download Total Annihilation. 

Once you have Total Annihilation installed, download the "Drop in" patch found on [TA universe](https://www.tauniverse.com/forum/showthread.php?t=46455). 

You can then simply just copy and paste the files in to the directory TA is installed to (By default it is: "/home/USERNAME/Games/gog/total-annihilation/drive_c/GOG Games/Total Annihilation"), make sure to overwrite existing files.

Next you need to download IPXwrapper this can be found [here](https://www.solemnwarning.net/ipxwrapper/). This too can be dropped in to the games root directory.

## Configuration

#### IPX wrapper config:
First, run the IPXwrapper config from the Lutis manager - by selecting Total Annihilation from the games library, then clicking the little wine icon and choosing "Run EXE inside wine prefix". navigate to the TA directory and find "ipxconfig.exe" and click on it, then perform the following actions:


  - Set Primary Interface to en1 (Check ipxwrapper.log to see what your ip address is under)
  - Set Network Adapters to en1
  - Check Enable Interface
  - Set Network Number to 00:00:00:01
  - Node Number will be autopopulated
  
  - Check Enable Windows 95 SO_BROADCAST
   - Check Automatically create Windows Firewall exceptions

#### Wine config:

Next in the Wine configuration, under Libraries tab add wsock32 in New override for library, and set it to use Native then Builtin under Edit Override
