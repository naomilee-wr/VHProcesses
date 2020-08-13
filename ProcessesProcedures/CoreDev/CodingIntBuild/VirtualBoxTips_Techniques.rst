:orphan:
|
|
|

=========================================== 
VirtualBox Tips and Techniques
===========================================

|

**Getting Started**
--------------------

This section covers steps needed to do to get the Virtual Machine (VM) up and running. 

|

**Creating the VM**
-------------------- 


- Be sure to give VM a large virtual disk! (It's a real pain to have to increase the size of an existing disk later on, although it can be done.)

  - Recommended size is 200 GB. 
   
- Give VM as many CPUs as it needs.

  - In most cases, use most (or all) of the hosts CPUs for best performance.
    
    - Example: For a quad-core host CPU that supports hyperthreading could give the VM 6, 7, or 8 CPUs.
    - A warning may be about "too many CPUs" because VirtualBox doesn't understand about hyperthreading and only counts the actual cores on the host. Ignore the warning. 
 
  - Limit how much of host's CPU time the VM can consume (to say 80% or 90%) to ensure the use of host for other things even if the VM is doing compute-intensive operations. 
  
- Give VM as much RAM as it needs.

  - If the host has 16 or 32 GB RAM, then give the VM at least 8 GB. 

- Make the VM's network adapter a "Bridged Adapter".
  
  - This ensures that the VM can access the network the same way the host itself does  
  - The default "NAT" type will allow the VM to access the network, but it may have problems accessing certain parts of the network (e.g. accessing certain areas under /folk or /net) because the Wind River network is set up to reject connections that don't come from privileged ports (i.e. from port numbers > 1024). Use NAT if required, but only if VirtualBox is used to configure the VM's network interface to use a privileged port for NFS connections.  
  
- Enable shared clipboard and drag-and-drop features.

  - Copying stuff from the VM to a Windows host seems to work OK.
  - Problems copying stuff from Windows to VM (if VM is running with admin privileges) is because VirtualBox doesn't allow to copy from an unprivileged environment to a privileged one. 
  
|

**Booting the VM**
------------------

- Mention where the OS installation disk lives 

  - Be sure to assign the VM a standard Wind River <site>-<userid>-<identfier> host name. (Example: yow-jdoe-v1)
  
    - **Important:** Ensure the host name does not exceed 15 characters, otherwise Windows-based computers won't be able to reference it via DNS. (This is a Windows-specific limitation --- Linux-based computers can handle host names that are 16 or more characters.) If Wind River userid is 8 characters long (which is true for many people), then the "identifier" portion of the host name can't be more than 2 characters! 
  - Be sure to create the userid using the same name as the Wind River userid. 
  
- Once the OS is up, install the VirtualBox guest additions. 

|

**Aligning VM userid value**
-----------------------------

- Ensure that the numeric value of the VM userid matches the numeric value of regular Wind River userid. Failing to do this can make it difficult to access other hosts, files, and services elsewhere in the Wind River network!

  - Do this right away! The following procedure only changes the numeric values of the files in the VM home directory, so manually update the ownership of the files in other directories on the VM.
  - To find out what the numeric userid (uid) currently is, just issue the command "id". 
  
- Log in as an administrator that isn't the userid being changed.
  
  - If unable to log in as "root".  create a new administrator account, use it to change the numeric userid value, then delete the new administrator account. 

- Change the numeric value of the userid.    *usermod -u <value> <userid>*

  - If unaware of the Wind River numeric value is, set up access to files on the network (see below), then display their ownership (eg. "ls -l ") 

|

**Personalize the VM**
-----------------------

- Configure the editor.
  
  - May need to install the editor  
  - If emacs used, set up ~/.bash_aliases with "alias emacs='emacs -nw'" to keep emacs from popping up a new window when trying to edit a file. 

- Configure the default terminal profile.
  
  - Click on a terminal window, then select "Edit Profile Preferences" at top of screen.
  -  Suggestion: Use monospace 8 font, with black on white text. 
  
- Configure bash terminal prompt.

  - Edit ~/.bashrc so that PS1 uses the color of choice.
  - Suggestion: 00;36 is a pleasant teal color. 

- Disable auto-locking of the screen (since presumably locking the screen on the host).

  - Set screen inactive to "never" and turn lock off. 

|

**Configuring the VM's Network Access**
---------------------------------------

This section covers things needs to give VM access to the Wind River network.
  

**Configuring the Network Interface**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- VM can typically to obtain its IP address dynamically via DHCP.
  
  - By default Ubuntu configures a new network interface to use DHCP
  - IMPORTANT: If running a lot of VMs at the same time (rather than just one or two), contact the Ottawa IT folks first to ensure that set of DHCP-managed IP addresses are going to be depleted. (This has been a problem in the past!) 

- If VM requires a static IP address for some reason, contact the Ottawa IT folks first to obtain an authorized static IP address. 


**Configuring DNS**
~~~~~~~~~~~~~~~~~~~~~~~

- Edit /etc/hosts

  - If VM uses DHCP delete 127.0.1.1 line, if it exists (or comment it out with a leading "#").
  - If VM has a static IP address, change 127.0.1.1 vmname to staticaddress vmname.
  - IMPORTANT: This step is needed to ensure the VLM Client tool refreshes its display properly after locking or unlocking a VLM-controlled target. 
  
- Edit the IPv4 network settings for the VM's Ethernet interface. (It's easiest to use GUI.)
  
  - DNS servers: 128.224.144.130, 147.11.57.128

  - If desired, add: 147.11.57.133, 147.11.161.33, 147.11.161.34 
	
  - Search domains: corp.ad.wrs.com, wrs.com
  
    - Windows PCs supplied by Ottawa IT also use kk.wrs.com (as 3rd and last entry)
	
- After saving, activate new settings by using GUI to turn interface "off", then "on".

  - Enter the following command to confirm the DNS servers were applied correctly:
    
    - nmcli d list | grep DNS (Ubuntu 14.04)
    - nmcli d show | grep DNS (Ubuntu 16.04) 
	
  - Display /etc/resolv.conf to confirm the search domains were applied correctly. 
  

**Accessing files under/net**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Install the automount ("autofs") package.
- Add (or enable) the following line to /etc/auto.master:

  - /net -hosts 
  
- Add the following line to /etc/nsswitch.conf:

  -  automount: files nis 
  
- Restart automount services.

  - sudo service autofs restart 
  
- Try displaying /net/yow-lxfs01/yow-lxfs0105/teams directory to verify access is working properly. 


**Configuring NIS**
~~~~~~~~~~~~~~~~~~~~~~

- Install the yellow pages ("nis") package.

  - Note: Ubuntu 11 tries to set up NIS, but the ypbind operation doesn't succeed --- just let it time out and fail ... 
		
- Add the following lines to /etc/yp.conf.

  - domain swamp server 128.224.195.20
  - ypserver 128.224.195.21 
		
- Verify /etc/defaultdomain is set to the following (change it if necessary):
  
  - swamp 
- [Ubuntu 16.04 workaround] Fix a problem with NIS not working after installation.
  
  - sudo /bin/systemctl add-wants multi-user.target rpcbind.service

    - Take a look at https://bugs.launchpad.net/ubuntu/+source/rpcbind/+bug/1558196.
    - Fix is to configure systemd to invoke rpcbind rather than allowing nis.service to do it. 
	
- Restart NIS service.
  
  - sudo service nis restart [WARNING: this no longer seems to work --- might need to reboot!] 
  
- Verify things are working properly.

  - domainname (should return "swamp")
  - ypwhich (should return "yow-adnis1.wrs.com", or something similar)
  - ypcat auto.yow (should return list of home directory locations) 

**Accessing files under /folk**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- IMPORTANT: This step assumes "Accessing files under /net" step shown above has already been done
- Add the following lines to /etc/auto.master to allow access /folk (Ottawa) and /folk (Alameda) directories:
  
  - /folk auto.yow
  - /folk-ala auto.home 

- Restart automount services
  
  - sudo service autofs restart 

- Try displaying /folk/ and /folk-ala/ to verify access is working properly.
  
  - Some users have reported that access to /folk stuff doesn't work properly after rebooting the VM; a workaround is to restart the automount services manually (see previous bullet).
  - Another workaround is to specify "yp:auto." instead of "auto." in auto.master. 

|

**Sharing VM folders to Windows host**
---------------------------------------

- Install Samba packages on the VM (using sudo).
  
  - apt-get install samba samba-common python-glade2 system-config-samba gksu
  - touch /etc/libuser.conf
  -  The second command is a Ubuntu 16.04 workaround for a bug with system-config-samba. 

- Start Samba configuration tool

  - gksudo system-config-samba
  - Need to use gksudo since it uses a graphical interface. 
  
- Use Samba configuration tool to share folder(s) to see the host
  
  - Default server security is "User", which limits access to permitted users.
  - Set Samba user info so that username and password are the same as for Windows PC (otherwise enter name/password when first trying to access folder from Windows, because the one Windows passes in won't match what Samba expects).
  - Set shared folder to be visible, writable, and accessible by Windows PC username. 

- On the host, map network drive to \\VM's_IP_address\folder_name.

- To prevent Samba from turning on a file's "execute bit" if to edit it from Windows:

  - Edit /etc/samba/smb.conf (requires "sudo" access)
  - Add the line "map archive = no" (add it under ["username"], but [global] might work too)
  - Save file, then restart the VM to ensure Samba uses the new info.
  - Note: Apparently the default behavior for Samba is to use the execute bit as the equivalent of the archive bit used by Windows file systems (which tells backup software that a file has been modified since the last archive and needs to be backed up). 

|

**Maintaining VM**
-------------------

This section describes how to keep VM running smoothly.

**Cloning a VM**
~~~~~~~~~~~~~~~~~~

- If cloning an existing VM, be sure to re-initialize the MAC addresses of its NICs inorder to be able to co-execute with the original VM (or other VMs).
        
  - IMPORTANT: This creates a new network interface, so need to configure its type, IP address, and DNS info. It won't inherit this from the existing network interface! 
  

**Fixing problems with VirtualBox guest additions**
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Sometimes after updating Ubuntu VM software, the guest's mouse and/or screen size functionality may not work.
        
  - To correct this, try reinstalling VirtualBox's guest additions. 
- If having trouble getting the mouse to point properly within the VM screen:
        
  - Look under the VM's "Input" menu and select "Mouse Integration" --- this should give mouse control to the VM only.
  - To give mouse control back to the PC enter the usual mouse control transfer key (usually Right Ctrl). 

- Be sure the guest additions CD is available to the VM.

  - Look under the VM's "Devices" menu. If necessary, eject what is already there and then select "Insert Guest Additions CD Image ...".
    - Alternatively, shut down the VM then open the VirtualBox app. Look at the "Storage" section for the VM-hopefully it says "VBoxGuestAdditions.iso". If not, click on the disk name and then remove it from the VM. Restart the VM and try inserting the guest additions CD. 

- If the Guest Additions CD doesn't run automatically, invoke it manually.

  - sudo bash
  - cd /media/<username>/VBOXADDITIONS_<version>
  - sh autorun.sh

- Once the guest additions have been reinstalled be sure to restart the VM.

  -  Things should now be working properly once again. 

|

**Using an Ottawa IT-supplied VM**
------------------------------------

Check with Ottawa IT to create an Ubuntu 14.04 VM. They'll create a machine named something like yow-<username>-lx and store it at yow-itcs/Images/VMs. It looks like they'll create a root account (password is P@ssw0rd) as well as normal Wind River account (using current CORP password). Once Vm is copied to host and fired up, the VM will already have guest additions installed and will be able to access the Wind River network (including files under /folk and /net.

- IMPORTANT: By default, a VM hard disk size of 100 GB is givern --- if a larger disk is required, specify this when submitting request to Ottawa IT. The Ottawa IT team will also only configure the VM with a single CPU, but can easily change this yourself once the VM is available. 

*If in a hurry:*

If the Ottawa IT  is unavailable, clone an exisiting VM created for someone else and then adapt it. The steps involved are:

1. Open VirtualBox, then add one of the VMs found under yow-itcs/Images/VMs. (YOW-UBUNTUBASE-LX has a 100GB disk.) Don't start this VM!
2. Clone the VM added, being sure to change the MAC address of its network interface and to rename the VM.
3. Remove the original VM from VirtualBox, but don't delete its files! 
4. Change the new VM's settings for preferences. (i.e. number of CPUs, amount of RAM, amount of video memory, etc.)
5. Fire up the VM. (Mention in VirtualBox the host's network adapters to be used for its network interface.)
6. Log in as "root", then create a userid (specifying normal Wind River userid and numeric id). Delete any other unwanted userids.
7. Rename the VM to the name to use (such as yow-YOURNAME-lx) by editing /etc/hostname and /etc/hosts.
8. Edit /etc/hosts as described in the first bullet of "Configuring DNS" above to ensure the VLM Client tool will work properly.
9. Reboot the VM and log in using the userid.
10. Verify the VM has the name specified and can access the network properly (including stuff under /folk and /net). 

|

**Change Log**
--------------
+----------------+----------------+----------------+----------------+---------------------------------------+
| **Date**       | **Change       | **Version**    | **Change By**  | **Description**                       |
|                | Request ID**   |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+
| 06/25/2020     | N/A            | 0.1            | Shree Vidya    | Transferred content from VirtualBox   |
|                |                |                | Jayaraman      | Tips and Techniques Twiki page        |
+----------------+----------------+----------------+----------------+---------------------------------------+
|                |                |                |                |                                       |
+----------------+----------------+----------------+----------------+---------------------------------------+

