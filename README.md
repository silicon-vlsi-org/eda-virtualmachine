# ABOUT
Setting up Virtual Machines (Virtual Box) and setup open source EDA tools


# INSTALLING LXLE ON VIRTUAL BOX

This section contains instruction on how to download and isntall Virtual Box (Virtual Machine) on a Windows/MAC/etc machine and then install a lightweight Ubuntu-based Linux distribution called LXLE.

- Download **Virtual Box** from http://www.virtualbox.org  for your particular desktop (Windows/Mac/etc)
  - Install it using the default settings.
- Download the **Linux distribution LXLE** from   http://www.lxle.net/download  appropriate for your system (32-bit/64-bit).
  - The download will be a CD/DVD image called an **ISO image** (eg. lxle-18043-64.iso) that you save it on your computer (eg. C:\Users\<username>\Downloads)
- Follow the steps below or check [this PDF](https://www.dropbox.com/s/2lovix0ntsw8yfw/2020-0917-Open%20Source%20EDA%20Setup.pdf) for step-by-instructions with screenshots.

**CREATING A NEW VIRTUAL MACHINE**

- Start Virtual Box and click `New` and fill the required information
  - Name: <ANY NAME>
  - Machine Folder: (Default is fine)
  - Type: `Linux`
  - Version: Ubuntu (64-bit) [Make sure your OS is 64-bit]
- Select the size of the **RAM** (> 2GB recommended but >1GB should be usable) 
- For **Hardisk** (recommended size 20G) select the following option:
  - `Create a virtual hard disk` and select `Create`
- Hard disk file type: `VDI (VirtualBox Disk Image)`
- Storage on physical hard disk: `Dynamically allocated`
- File location and size:
  - Select the location of the file and
  - the size (eg. 20GB)
- Now your Virtual Machine is configured and ready to be host an operating system (OS).

**INSTALLING LINUX ON THE VIRTUAL MACHINE**

- Before starting the installation, load the ISO image (eg. lxle-18043-64.iso) in the optical drive:
  - Open Virtual Box and select the new virtual machine just created and select `Settings-> Storage -> Controller:IDE` and select `Add optical drive` and browse to location where the linux ISO file is and select it.
- Now start the Virtual Machine.
- From the linux install menu, select `Install - start installer directly`
- Select the required Options: 
  - Language: `English`
  - Updates and other softwares: `Download updates while installing LXLE`
    - **NOTE**: If you have slow or no internet connection then deselct this.
  - Installation type: `Erase disk and install LXLE`
  - Write changes to the disk: `Continue`
  - Select time zone
  - **USERNAME** (Who are you?):
    - Your Name: <ANY NAME>
    - Your computer's name: Suitable name
    - Pick a username: <Choose a simple username without any special character>
    - Password: **IMPORTANT: Keep the password safe. If you lose it, you cannot reset it.**
- After selecting all options and selecting continue, it will take a while to install the OS.
- After the installation is complete you will be asked to reboot and after the VM comes up, you will see the login window. Enter the set password to login.
- After loging in, start terminal window by clicking the application `sakura` from the top-left menu.
- Since the Linux OS image does not have all the updates, it's recommended you update the Linux OS in two steps by typing the following two commands in the terminal window:
  - `sudo apt update`
  - `sudo apt upgrade` (Type `Y` to confirm)
    - **NOTE** The first update will like download 400-500MB of data so make sure you have a good internet connection.
    - During the upgrade process, whenever you get the message to `keep or overwrite` a configuration file, choose to **keep** it.
- After successfully updating the OS, install some of the essential software packages:
  - `sudo apt install build-essential vim git`
  
