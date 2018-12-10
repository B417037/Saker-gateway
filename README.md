# Saker-gateway initializing it as a border-router
Setting up of Saker gateway as a 6LoWPAN border-router

Step 1:
Download ubuntu(16.04 version or higher)
if you do it on a virtual machine:
•	download ubuntu
•	extract the zip file(or RAR file)
•	download VirtualBox
•	install VirtualBox with default settings.
•	Open VirtualBox and click on new
•	Name:Ubuntu   Type:Linux
•	version:Ubuntu
•	click on next
•	set memory size to be 4GB
•	click on next
•	select - create virtual hard disk now and hit on Create.
•	select virtual box disk image(VDI) and hit next.
•	type Ubuntu(10GB) in the name coloumn and press create.
•	select the folder for the iso image(amdk file-1.51GB) of ubuntu 64 bit(in downloads section--where you extracted the ubuntu software.)
•	let the system to boot.
•	select the desired language and install ubuntu with default settings.-->just press next-->dont select any option click on continue.
•	no options to be selected click on install now.
•	let the system to install.
•	restart the machine.
•	select the timezone and keyboard language.
•	Ubuntu in VirtualBox is now set.


Step 2:
•	open Ubuntu(16.04 or higher).
•	Download GNU ARM Toolchain version 7.link-->
https://developer.arm.com/open-source/gnu-toolchain/gnu-rm/downloads
•	extract the file in downloads.
•	make a new folder named 'opt' in the home folder.
•	copy the extracted file in the opt folder.
•	open Ubuntu terminal (Ctrl+Alt+T)
•	in the terminal type-->
 	 'cd opt' and hit enter(without  ' '  XD)
  'chmod -R -w "${HOME}"/opt/opt/<name of extracted file in opt folder>' and hit enter (include " " in $HOME)
•	you will notice a lock on the copied folder in opt.
•	make another folder say weptech in the home folder.
•	open the terminal and type-->
    	'cd weptech' and press enter
    	'git clone https://github.com/Weptech-electronik/contik.git ' and press enter
    	'cd contiki'  and press enter
    	'cd examples'  and press enter
    	'cd saker'  and press enter
    	'cd ip64-rpl-border-router'  and press enter
    	'gedit project-conf.h'
•	change the status of CC1200 from 1 to 0 and save the file.
•	in the terminal type- 'make TARGET saker'  and press enter.
    	'sudo apt-get install gcc-arm-none-eabi'  and press enter
    	'sudo apt-get install python-serial'  and press enter.
    	'git submodule update--init'  and press enter.
    	'sudo apt-get upgrade'  and press enter.
    	'sudo apt-get update'  and press enter.
    	'make TARGET=saker'  and press enter.
    	'make TARGET=saker border-router.bin border-router.upload'.
 Step 3:
•	connect ethernet cable
•	'make TARGET=saker connect router' press the reset button.
•	copy IPv4/IPv6 address and paste it in browser.
  
