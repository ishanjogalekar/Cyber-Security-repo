# ✔Types :

1. Using Hypervisors like virtual box or VMware virtual environment .
2. Dual boot on HDD only.
3. Kali Linux Bootable pen-drive (Live Persistence). 
4. Latest Windows can enable Linux subsystem . Kali Linux subsystem.

# 💻Hypervisor installation : Virtual box / VMware <br>
Choose anything but prefer to use virtual box . Here only virtual box installation is mentioned.

### 1.Virtual box : 

Go to **virtual box** website link given below . There is no special requirements needed for it . Also download extra plugin package with it.

**Link** :  [VirtualBox](https://www.virtualbox.org/)
<br>

### 2.VMWare :

Go to VMWare website link given below. 
<br>Download VMWare workstation.Some features may be paid.<br> 
So it is less recommended than **Virtual box**. 

**Link** :  [VMWare](https://www.vmware.com/in.html) 

## Kali Linux :
Download Kali Linux ISO file from given Link.<br> Please download it from official website.<br>
**It is free.**

**Link** :  [Kali Linux](https://www.kali.org/downloads/)

1. For virtual box download 64 bit Installer file ISO.
2. For USB boot / Dual boot download Live file .

### Kali Linux installation platforms :

![Image](https://github.com/ishanjogalekar/Cyber-Security-Notes/blob/main/Images/k.png?raw=true)

- Install Virtual box / VMWare on your PC . Then you can install Kali Linux on virtual machine.

# Creating Virtual machine & Installing Kali on Virtual box :

### A.Creating Virtual Machine  :

1. Open your virtual box application & click on "New".
2. Give Name to machine & choose path for it (do not use drive where OS is installed / most C drive) 
3. Choose type  **"Linux"** and then choose **"Debian 64 Bit"**.
4. Choose default option given there. Dynamically allocated physical Hard disk.
5. Choose RAM size & HDD size as given there (give exactly recommended value).
6. Now your virtual machine is created .

 
### B.Installing Kali Linux OS in Virtual machine (Booting) : 

1. Now we have to load Kali OS in it, for that click on settings.
2. Uncheck Floppy and move it down in system . Give processors (recommended 3 for Intel i5 8th gen processor) & increase  display memory ).
3. Choose copy paste and move option as **Bidirectional**. Check network adapter is on **NAT** .  
4. Go to storage → Controller : IDE → Choose ISO file → Kali Linux (where you downloaded ISO file choose that ISO file ).
5. Press OK and then Start  virtual machine.
6.  Follow Instructions on Kali Linux :<br>
      a. Choose Graphical Install.<br>
      b. Choose language & location.<br>
      c. Choose keyboard layout.<br>
      d. Give Username , password .<br>
      e. For partition on hard disk give as it default.(recommended settings)<br>
      f. Install Grub boot loader (default settings).<br> 
      g. Once it is down machine will restart and Kali Virtual Machine will be run .

## Note : 
Sometimes there is problem with GUI means black screen installation of Kali in V Box :<br>
To solve this steps are →
1. First login to kali then black screen will appear that is actually terminal window.
2. Type - **Command** :  cat  /etc/apt/sources.list
3. Then type **Command** : sudo nano/etc/apt/sources.list.<br>
It will first ask password of Kali and then open nano text editor .
4. At the end of document type→ 

        deb [http://http.kali.org/kali](http://http.kali.org/kali) kali-rolling main non-free contrib

        deb [http://http.kali.org/kali](http://http.kali.org/kali) kali-rolling main non-free contrib

5. Save file by pressing ctrl+o and ctrl+x .

6. Then type sudo apt-get update . This will take time. Take short break for that.

7. After process done . Type sudo apt-get install gdm3

8. After installation it will ask 2 options  **gdm**  or **lightdm** . Choose anyone.

9. Type **init 6** to restart. Now it will correct GUI and you can see full kali Linux OS.

 **Note :- All these process requires network connection.**

**Video tutorial link** : [Youtube Tutorial](https://youtu.be/JNyxlOx97ZY)

# 📀Installation Of Kali Linux on Windows directly : WSL (Only for windows host)

- WSL is Windows sub system Linux.
- Some Linux operating systems can be installed directly in windows eg : Ubuntu , Kali etc.

### Follow the steps to install Kali WSL 

1. **INSTALL WSL 2** :  First  RUN POWERSHELL as administrator  ( search  for powershell in search bar and click run as administrator.) 

⌨️ **Command** :  
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

2.  RESTART computer  then again type in powershell

**⚙Commands :** 
      
    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart



  3. **Download Linux Kernel**: [Linux Kernel](https://aka.ms/wsl2kernel)

  4. Then go to Microsoft store and install kali. <br>
**Refer Image below** ->
        
![M Image](https://github.com/ishanjogalekar/Cyber-Security-Notes/blob/main/Images/m.png?raw=true)

 5. This  will install terminal of kali in windows.

 6. **SET DEFAULT TO WSL 2** <br>
**command** :  wsl --set-default-version 2 <br>
**CHECK VERSION**<br>
**command** :  wsl --list --verbose

7. INSTALL GUI: <br>
Open Kali Linux terminal and type the following commands this requires network connection.

**Command** : 

    sudo apt update && sudo apt upgrade -y
    sudo apt install kali-desktop-xfce -y  / sudo apt install -y xfce4

### XRDP server :
**Command** :  
            1.sudo apt install xrdp -y<br>
            2.sudo service xrdp start

If there is **problem** this command will fix :-<br>
sudo umount -f thinclient_drives


8. Now in terminal type - <br>
    **Command**: sudo ifconfig <br> 
and note down ip address information.

9. Now in windows search for **remote desktop**:  

        a. In connection menu type ip address you noted down.

        b. It will take time to connect keep kali terminal running.

        c. It will ask password to login.

10.  WSL uses host machine resources. sudo in front of each command will ask user password first. 
while  running kali terminal first time it will ask to set password.

## Important Links:

**Link** :
[Win-Kex Documentation](https://www.kali.org/docs/wsl/win-kex/)

**To install kali full version , type in terminal  : (default minimal)**
     
    sudo apt install kali-linux-large

**WSL link :**
[WSL Microsoft Documentation](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

#### Note :  WSL requires at least 30 GB memory space in Main Drive. where host OS is installed mostly C drive.

**Internet connection problem** : (If network is not showing in Kali)<br>
Open windows cmd in admin mode and type these **⚙commands**:

    1.netsh winsock reset
    2.netsh int ip reset all
    3.netsh winhttp reset proxy
    4.ipconfig /flushdns
    5.reboot

# 📍Installation On USB Drive

This need Liver version on kali Linux.<br> 
Also it needs one USB flashing / portioning software called as **rufus**.<br>
Also **balenaEtcher** is free and easy alternative for rufus<br> 
Minimum **16 GB USB drive** is required.

Links:- <br>
1.[Rufus](https://rufus.ie/en/)<br>
2.[BalenaEtcher](https://www.balena.io/etcher/)

Video tutorial:- [Youtube Tutorial for USB Boot](https://youtu.be/n2olKupv9fY)
