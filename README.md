##  Basics

### vim editor

 - `vim <file-name>` Open a file
 - `ESC` To enter `Normal` Mode
 - `:w` To save the file. Use this command only if you are in 'Normal` mode
 - `:q` To exit out of the eidtor. This also works in `Normal` mode.
 - `:q!` To quit Vim without saving the data file (all unsaved changes are discarded).
 - `:set number` To show line numbers
 - `vim <direcotry-name>` Opens Vim explorer.
 - `/` Search Pattern/Word.

## Network:

 - `ifconfig` => shows the network adapter details
 -  `ip a` => kinda does the same thing ifconfig does
 - `iwconfig` => ifconfig but for wireless adapters
 - `arp -a` => Associates ip addresses with MAC addresses.
 - `netstat -ano` => shows all the ports that are open and what is connected to them.
 - `route` => shows our routing table
 - `Ping <destination>` Test connectivity between current user and destination.
 - `ssh <username>@<hostname>` connect to a remote server Securely
 - `nmap <ip address range>` Port scanner which can also be used to find vulnerabilities
 - `traceroute <ip/website>` Shows all the router ips on the path between your machine and the website's server 

## Copying files

 - `rsync /from/path /to/path`
 - `-P` => progress bar
 - `-r` => recursive for dirctories

## Metasploit

 - `msfconsole` Opens up metasploit which is a framework that allows us to attack other machines using known vulnerabilities
 - `msfsearch <keyword>` Searches for known exploits related to that keyword
 - `msfvenom -p <payload>` Allows us to create specific payloads that can be sent to a victim's machine to exploit.


## Show off (Fun)

 - `cmatrix` shows text rain like matrix movie
 - `cowsay <text>`generates ASCII art picture of a cow with text input.
 - `hollywood`screws up your terminal and makes it look like movie hacking scene.
  //respective packages must be pre-installed in the system

## Bootable usb

 - `fdisk -l` list all the partition of storage medium - with this find out your usb name
 - `sudo dd bs=4M if=<path to iso> of=/dev/sdx<destination disk that is your usb> status=progress && sync
	 - progree will give you status bar
	 - sync is to clear the cache
	 - 4M means we pass the data in 4MB chunks (not sure)
 - `sudo wipefs --all /dev/sdx`
 - `sudo cfdisk /dev/sdx`
 	- dos, New, max size, primary, write, yes, quit (some options that will pop up)
 - `sudo mkfs.vfat -n <name> /dev/sdxy`
 	- here we have to include the `y` which is the partition name
