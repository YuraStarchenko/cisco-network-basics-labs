# Packet Tracer – MAC and IP Addresses

## Description

This lab shows how MAC and IP addresses work in a local network and a remote
network. We use Simulation mode in Cisco Packet Tracer to watch PDU packets.

No configuration is needed.

## Objectives

See MAC and IP addresses in a local network

See how a router works with remote networks

Understand the default gateway

Check PDU details

## Part 1: Local Network

Steps

Open Command Prompt on PC 172.16.31.3

Run: ping 172.16.31.2

Switch to Simulation mode

Click the PDU envelope

PDU Information

Source MAC: 0060.7036.2849

Destination MAC: 000C.85CC.1DA7

Source IP: 172.16.31.3

Destination IP: 172.16.31.2

Result

<!-- <p align="left">
   <img src="/lab05-home-network/screenshots/Screenshot1-2.png" width="700">
  <img src="/lab05-home-network/screenshots/Screenshot1-1.png" width="700">
</p> -->

![Home Network Setup](/lab05-home-network/screenshots/Screenshot1-2.png){:width="700px" align="left"}
![Home Network Setup](/lab05-home-network/screenshots/Screenshot1-1.png){:width="700px" align="left"}

PCs talk directly No gateway is needed

## Part 2: Remote Network

Steps

From PC 172.16.31.3 run: ping 10.10.10.2

Use Simulation mode

Click the PDU envelope

PDU Information

Source MAC: 0060.7036.2849

Destination MAC: 00D0.BA8E.741A (router)

Source IP: 172.16.31.3

Destination IP: 10.10.10.2

Result

![Home Network Setup](/lab05-home-network/screenshots/Screenshot2-1.png)

Traffic goes to the router MAC address changes IP address stays the same

## Key Points

MAC address = Layer 2 IP address = Layer 3 Gateway is needed for remote networks

## Status

Completed Simulation tested
