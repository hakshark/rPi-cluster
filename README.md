<p align="center"><img src="https://raw.githubusercontent.com/hakshark/rPi-cluster/master/images-icons/pi-logo.jpg" height="73" alt="Raspberry Pi Logo" /></p>

# rPi-cluster: A learning platform

A cluster ([Bramble](http://elinux.org/Bramble)) of 5 Raspberry Pi nodes onto which Docker and Portainer are deployed.

## Why

to assist in my learning of a variety of container based applications. 

This has been inspired by the efforts of people like Jeff Geerling () and Don Hui () who without their excellent guidance I would remain in ignorance.

## Specs - WIP

  - 16+ ARMv7 CPU Cores
  - 5.6 GHz combined compute power
  - 4 GB RAM
  - 128 GB microSD flash-based storage
  - 1 Gbps private network with PoE

## Setting up the Pis

The process for setting up all the Raspberry Pis is outlined in the Wiki:

  1. Prepare the Raspberry Pis for provisioning
  1. Rack the Raspberry Pis
  1. Network the Raspberry Pis
  1. Provision the Raspberry Pis
  1. Deploy Docker to the Raspberry Pis
  1. Create Docker Swarm
  1. Deploy Portainer onto Master Node

> It is recommended you use the 64-bit version of Raspberry Pi OS, as some of this project's dependencies require it (and may not install on 32-bit Pi OS).
