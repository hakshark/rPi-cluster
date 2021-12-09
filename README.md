<p align="center">
  <img src="https://raw.githubusercontent.com/hakshark/rPi-cluster/master/images-icons/pi-logo.jpg" height="73" alt="Raspberry Pi Logo" />
  <img src="https://raw.githubusercontent.com/hakshark/rPi-cluster/master/images-icons/pi-logo.jpg" height="73" alt="Raspberry Pi Logo" />
  <img src="https://raw.githubusercontent.com/hakshark/rPi-cluster/master/images-icons/pi-logo.jpg" height="73" alt="Raspberry Pi Logo" />
  <img src="https://raw.githubusercontent.com/hakshark/rPi-cluster/master/images-icons/pi-logo.jpg" height="73" alt="Raspberry Pi Logo" />
  <img src="https://raw.githubusercontent.com/hakshark/rPi-cluster/master/images-icons/pi-logo.jpg" height="73" alt="Raspberry Pi Logo" /></p>

# rPi-cluster: A learning platform

A cluster ([Bramble](http://elinux.org/Bramble)) of 5 Raspberry Pi nodes onto which **Docker** and **Portainer.io** are deployed to create my learning platform.

## Why

This is to primarily assist in my learning of a variety of container based applications, and to have it bit of fun. 

This has been inspired by the efforts of people like **Jeff Geerling** ([geerlingguy](https://github.com/geerlingguy)) and **Don Hui** ([novaspirit](https://github.com/novaspirit)) who without their excellent guidance I would remain in ignorance.

## Cluster Specs - WIP

  - 5 x [Raspberry Pi 4 Model B](https://thepihut.com/collections/raspberry-pi/products/raspberry-pi-4-model-b) (4GB, 1.5GHz 64-bit quad-core CPU) - if you have 8GB variants, more power to you!!
  - 2 x [8-Slot Cloudlet Cluster Cases](https://thepihut.com/collections/raspberry-pi-cases/products/8-slot-cloudlet-cluster-case)
  - 1 x [Argon ONE M.2 Raspberry Pi 4 Case](https://thepihut.com/collections/raspberry-pi-cases/products/argon-one-m-2-raspberry-pi-4-case) **8TB maybe**
  - 1 x [WD Green 240GB M.2 Internal SSD](https://thepihut.com/collections/raspberry-pi-sd-cards-and-adapters/products/wd-green-240gb-m-2-internal-ssd) (for the Argon ONE Raspberry Pi)
  - 4 x [WD Green 240GB 2.5" SSD](https://thepihut.com/collections/raspberry-pi-sd-cards-and-adapters/products/wd-green-240gb-2-5-ssd) **8TB to be added when they finally arrive**
  - 4 x SSD to USB 3.0 Cable for Raspberry Pi
  - 1 x TP-Link 8-Port Gigabit Network Switch (**this build is NOT using Power-over-Ethernet (POE)**)
  - 5 x Cat6A Shielded Snagless RJ45 Ethernet Cable
  - 1 x Anker Compact 60W 10-Port USB Charging Hub
  - 5 x USB C 3.0 to USB 3.0 Cable 5Gbps Right Angle 90 Degree 3A
  - 1 x M.2 NVME to USB C Enclosure External USB 3.1 to PCI-E (M KEY) for flashing O/S onto M.2 SSD  

>**Note:** You could use microSD cards instead of the SSD drives, in that case you need to think about the speed and capacity of the cards, especially if your container apps are going to store large amounts of data.  

>**Note:** You could ommit the network switch and cables if you intend to use your wi-fi for connectivity. **No** instructions are provided to setup and configure wireless connectivity in this project.  

>**Note:** For my implementation I will be running all the Raspberry Pi's in this project headless (ssh and cli). You may prefer to use the GUI and therefore would need monitor, keyboard and mouse. **No** instructions are provided for setup and configuration through the GUI, although you could just open a terminal inside the GUI and try some of the install and configurations......

## Cluster Design - WIP

  - rPiManager - Fitted into the Argon ONE case, uses M.2 SSD to boot from and to store data
  - rPiDockNode01 - Docker worker node fitted into the Cloudlet Cluster case, attached to the 2.5" SSD to boot from and to store data
  - rPiDockNode02 - Docker worker node fitted into the Cloudlet Cluster case, attached to the 2.5" SSD to boot from and to store data
  - rPiDockNode03 - Docker worker node fitted into the Cloudlet Cluster case, attached to the 2.5" SSD to boot from and to store data
  - rPiDockNode04 - Docker worker node fitted into the Cloudlet Cluster case, attached to the 2.5" SSD to boot from and to store data

## Software & Utilities- WIP

  - Raspberry Pi O/S 64-bit ([raspios-bullseye](https://downloads.raspberrypi.org/raspios_arm64/images/))
  - docker (to be completed)
  - portainer (to be completed)
  - [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
  - ssh client (PuTTY and MPuTTY)

>**Note:** It is recommended you use the 64-bit version of Raspberry Pi OS, as some of this project's dependencies require it (and may not install on 32-bit Pi OS).

>**Note:** You could potentially use other ARM-based Linux distros, but I have not had chance to look into these

## Building the rPi-cluster

The process for setting up all the Raspberry Pis is outlined in the Wiki:

  1. [Prepare the Raspberry Pis for provisioning](https://github.com/hakshark/rPi-cluster/blob/main/setups/pi-Step1.md)
  1. Rack the Raspberry Pis 
  1. Network the Raspberry Pis h
  1. Provision the Raspberry Pis
  1. Deploy Docker to the Raspberry Pis
  1. Create Docker Swarm
  1. Deploy Portainer onto Master Node
