# IPv6-Lab

## Initial situation

In this project, a laboratory for IPv6 will be set up using a desktop computer with a current Debian system. To use the computer furthermore for its actual purpose, this should be done as far as possible without stirring up a lot of dust (e.g. using various outdated network backends).

OS: Debian GNU/Linux 12  
Kernel: 6.1.0-18-amd64  
Network backend: NetworkManager  
Hypervisor: KVM  
Virtual switch: Open vSwitch 3.1.0 

## Required packages

- openvswitch-switch
- gvncviewer

## Network topology
![Network topology](img/lab2.png)

## Configuring the bridge 
Info about current connetions

    # nmcli con show

Add bridge

    # nmcli con add type bridge ifname labBridge0

Add interface to the bridge

    # nmcli con add type bridge-slave ifname wlp4s0 master labBridge0

Turn on the bridge

    # nmcli con up bridge-labBridge0


