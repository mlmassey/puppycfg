PuppyMan
  
Version: 1
  
Date: 2012-9-17  



Puppyman is a portable Linux distribution based on Puppy Linux that strives
to fit a full Linux development environment on a USB stick.  The goal is to
create a portable Linux development environment for Beaglebone software 
development anywhere you go.  

Just loading a Linux distro on a USB stick and booting from it won't really
work.  Loading and using a standard USB2 stick is very slow.  Puppy Linux 
solves the problem by running everything in memory off a LiveCD, making it
highly portable, fast, and compact.   



For more information on Puppy Linux, check out: http://puppylinux.org  




[KEY FEATURES]  

1. Optimized Linux environment based on Puppy Linux 5.2.8 (Lupu - Ubuntu 
Compatible)  

2. VirtualBox virtual machine, which is how I run it.  It could be made into
a bootable USB stick, but I find its easier to run in a virtual machine so I
can work on it in parallel with my normal environment  

3. Virtualbox guest additions have beeen installed and shared clipboard works great.
Automatic screen resize does not work, but can be adjusted by restarting xwin
and tweaking the xorg.conf  

4. Eclipse JUNO optimized for C/C++ is installed for development.  Configured
to cross-compile with Angstrom crosstools for Beaglebone development.  

5. Angstrom crosstools is included as an SFS, so it saves space  




[HOW TO INSTALL]  

1. Checkout the Git project to a clean USB stick  

2. Download the following additional SFS files for Puppy and put them in the 
root of the USB stick.  
The project will expect these files to be loaded at boot.  You can use the 
PET installer found on the desktop to download these:
  - Lupu LiveCD from http://puppylinux.org: lupu-528.005-iso
  - Java JRE (java_jre_6u22-Lucid-sfs4.sfs)
  - Puppy kernel source (kernel_src_L4-2.6.33.2-patched.sfs)
  - Lupu DEVX (GNU compiler for Puppy):lupu_devx_528-4.sfs
  
3. Download VirtualBox from http://virtualbox.org and install it.  You will
need to download the Extension package also for faster USB  

4. Import the Puppyman.ova as a new virtual machine into VirtualBox  

5. You should place the Lupu LiveCD somewhere on the local computer.  You can't
have it on the USB stick, since you need the stick to read/write your Puppy
save information.  I suggest you put it in the same directory as the virtual
machine is saved in.  

6. Configure the virtual machine to mount the LiveCD and keep it mounted.  You
can find this under Settings>Storage and mount the ISO to the CD drive.  Make
sure to checkmark that it is a LiveCD  

7. Enable the USB filter to recognize the USB stick with your files stored on
it in VirtualBox.  You can do this by looking under Settings>USB and add a new
filter that recognizes your USB stick and automatically makes it available to 
the virtual machine on boot.  You need this to again read your Puppy save 
information.  
8. Start your virtual machine and presto!  




[INSTALLED PACKAGES]  

1. Puppy devx  

2. Java-JRE SFS
  
3. Eclipse Juno (http://www.eclipse.org)  

4. Angstrom Linux crosstools  

5. Google Chromium (browser)
  
6. Virtualbox Guest Additions
  
7. Nano (text editor)
  
8. Git 1.7
9. SSH
10. SSL
11. Additional smaller packages (see Puppy Package installer)