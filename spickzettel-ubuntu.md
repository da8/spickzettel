
# check if package is installed
* apt -qq list PACKAGE

# gnome-tweaks - issues with starting it
* first attempt to solve it
    * sudo nano /etc/apt/sources.list
    * add the following lines
        * deb http://security.kali.org/kali-security kali/updates main contrib non-free
        * deb http://http.kali.org/ /wheezy main contrib non-free
    * Now save it, press Ctrl + x press Y press enter
    * Back in the terminal
        * apt-get update
        * apt-get install gnome-tweak-tool
    * Now issue gnome-tweak-tool in the terminal and it should open.
        * error
            * ImportError: cannot import name '_gi' from partially initialized module 'gi' (most likely due to a circular import)
* second attempt to solve the issue    
    * cd /usr/bin/
    * rm python3
    * ln -s python3.6 python3
* now starting gnome-tweeks works

# how to create zip file in pieces
* create split zip files 
    * zip -r -s 500m data.zip data/
* unzip files
    * merge split files  
    	* zip -s 0 data.zip --out unsplit.zip
    * unzip
        * unzip unsplit.zip  
# create and rund your first shell script (https://linuxhandbook.com/run-shell-script/)
    mkdir scripts
	cd scripts
	touch hello.sh
	vim hello.sh
	type in "echo 'Hello, World!'", save the file and exit vim
	chmod u+x hello.sh
	./hello.sh
	Hello, World!
# free up space in Ubuntu
* running out of disk space in ubuntu can lead to the system not booting
* check free space
	* command line
		* df -h
	* gui
		* Disk Usage Analyzer
* free space in Ubuntu (https://itsfoss.com/free-up-space-ubuntu-linux/)
1. Get rid of packages that are no longer required [Recommended]
	* sudo apt-get autoremove
2. Uninstall unnecessary applications [Recommended]
	* sudo apt-get remove package-name1 package-name2
3. Clean up APT cache in Ubuntu
	* check used space
		sudo du -sh /var/cache/apt
	* remove outdated packages
		sudo apt-get autoclean
	*  Or delete apt cache in its entirety (frees more disk space)
		sudo apt-get clean
4. Clear systemd journal logs [Intermediate knowledge]
	* check disk usage
		journalctl --disk-usage
	* The easiest for you is to clear the logs that are older than a certain days.
		sudo journalctl --vacuum-time=3d
5. Remove older versions of Snap applications [Intermediate knowledge]
	* check disk usage
		du -h /var/lib/snapd/snaps
	* create a bash script with the following code and run it
		#!/bin/bash
		# Removes old revisions of snaps
		# CLOSE ALL SNAPS BEFORE RUNNING THIS
		set -eu
		snap list --all | awk '/disabled/{print $1, $3}' |
			while read snapname revision; do
				snap remove "$snapname" --revision="$revision"
			done
6. Clean the thumbnail cache [Intermediate knowledge]
	* check disk usage
		du -sh ~/.cache/thumbnails
	* free space
		rm -rf ~/.cache/thumbnails/*
7. Find and remove duplicate files
	* gui
		sudo apt install fslint
	* command line
		* install it
			sudo apt install fdupes
		* search duplicates
			fdupes /path/to/folder
			fdupes -r /home
		* delete duplicates
			fdupes -d /path/to/folder
		
		
		
