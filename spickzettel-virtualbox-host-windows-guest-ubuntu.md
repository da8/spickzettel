
# increase disc size of a virtual machine when host is Windows 10 and guest Ubuntu while lvm is being used
	* check if lvm is used
		* command line
			cat /etc/fstab
			Watch the line with your root filesystem. The indicator for LVM would be somethinkl with /dev/mapper/....
		* gui
			Check the partitions with GParted. Partions with LVM will have the lvm flag.
	* Resize the disc size in Windows 10
		* Select the VM machine
		* Goto File > Virtual Media Manager
		* Choose the right virtual disc (VM Name.vdi or something similar)
		* Increase the disc size for the vm and the snapshoots to the desired size and apply it
	* Modifications in Ubuntu
		* Restart the vm
		* Use GParted to resize root parttion
		* reboot the system
		* make the lvm partitioning scheme aware of the changes made
			* as the root user run the commands
				* sudo su
				* pvs
					* check for the right partition XXX 
				* pvresize /dev/XXX
				* lsblk
					* Running lsblk shows that the root partition is still occupying only ZZZ whereas there’s YYY on the partition XXX. This is because our physical partition has grown but the logical volume manager is not aware of this.
				* enter lvm 
					* lvm 
					* lvm > lvextend -l +100%FREE /dev/ubuntu-vg/root
					* lvm > exit
				* resizefs /dev/ubuntu-vg/root
		* finally the space should be available
		* df -h
* resources
	* [Increase VirtualBox Disk Size](https://linuxhint.com/increase-virtualbox-disk-size/)
	* https://askubuntu.com/questions/1106795/ubuntu-server-18-04-lvm-out-of-space-with-improper-default-partitioning
	* https://askubuntu.com/questions/202613/how-do-i-check-whether-i-am-using-lvm
