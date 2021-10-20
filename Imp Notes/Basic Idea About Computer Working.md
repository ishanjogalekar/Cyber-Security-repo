# 🌎Basic Idea About Computer Working

## ⚙ Basic structure :


There are three main units in PC, Input → Processor → Output Input and output devices are peripherals.
The processor is mainly ALU ( Arithmetic Logic Unit). The processor also consists of some memory Primary memory, apart from that
there are secondary memory units also. All components are placed over the motherboard which is the main chip and components are connected to each other with BUS (wires).

[img1 text](https://i.ibb.co/F6879Xm/Presentation1.jpg)
### ALU :

Most computer operations are done in this part. 
Load operands into memory, bring them to the processor from memory.
ALU stores the result of any program, calculations to memory.
Control Unit in processor controls all operations.

### GPU :

It is a graphical processes unit. These are the most advanced processors mainly
dedicated to graphical processing. It is optimized for graphical calculations. It is a stronger version of the CPU.

### Network Interface controller :


It is a controller for all network environments of PC.
Mainly there are two interfaces 1.Ethernet    2.WIFI

### OS component :


OS is the operating system of a PC. It is basically an environment for all operations of computers.
There are almost 5 types of OS.
Popular OS for computers are:-
a. Windows 
b. Linux based OS 
c. MAC (ios)
Kernel - Core code part of OS, which boots OS in memory.
File system - Access the files in HDD and file handling operations.
User Interface - CLI emulators, Outlook for windows.
Networking - Network drivers.


## Virtual Systems:-

Virtualization is an act of creating a fake environment within another system for executing different programs. Installing Kali in the V box in the Windows system is an example of virtualization. It is very useful for limited hardware & testing, usage purposes.

**Benefits** :
1. Efficiency - More efficient restoration, distraction & usage of resources.
2. Cost - Cost is reduced on hardware.
3. Redundancy - Easier to Backup.
4. Versatility - Simultaneously you can use two OS or more.

## Hypervisor:-

Piece of software capable of virtualizing hardware components & maintaining the virtual environment.
**Host machine**: Host machine is main, basic hardware where hypervisor installed.
Bad idea to give more resources to the hypervisor from the host machine. Give recommended only.
**Guest machine**: Virtual environment installed in the hypervisor. Mostly another OS.

## 🎱 Types Of Hypervisors:-

1. Type 2 :
Application hypervisors run on top of the installed OS & host the virtual environment on top of the host kernel. Best for usage and also it is very efficient.
Recommended using this.
Examples → Microsoft Virtual PC, Oracle Virtual Box, VMware Workstation, Oracle Solaris Zones, VMware Fusion, Oracle VM Server etc.
2. Type 1 :
Bare metal hypervisors special computer run the hypervisors as OS
itself. Dedicated for virtualization. It is not for special services or GUI like it is not useful for running applications on it.
Example → VMware ESXi, Microsoft Hyper-V, Apple Boot Camp, XEN servers for Linux systems.


[img2 text](https://i.ibb.co/8d2zB7S/pre-2.png)

**Kernel integrated hypervisors** :
Hyper-V platform is free to prebuild with Windows servers, running on Windows kernel, easy to use. KVM another Linux based kernel preloaded hypervisor, free to use, developed by the Red Hat organization.

## Working Of Hypervisor :

Works by allocating resources from the host machine to the guest machine. The resources include drive space, RAM & network. RAM & hardware, drive space are represented by files on the host machine while the network is actual hardware.



