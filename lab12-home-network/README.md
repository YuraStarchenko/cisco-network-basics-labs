# Packet Tracer – Using the ipconfig Command

<p align="left">
  <img src="/lab12-home-network/screenshots/Screenshot1.png" width="700">
</p>


## Objectives

* Use the **ipconfig** command to find a wrong PC configuration.

## Scenario

A small business owner cannot access the Internet from one of four office PCs.
All PCs use **static IP addresses** in the **192.168.1.0 /24** network.
The PC must access the web server **[www.cisco.pka](http://www.cisco.pka)**.
Use **ipconfig /all** to find the incorrectly configured PC.

## Instructions

### Part 1: Check Configurations

* On each PC, open **Command Prompt**.
* Run:

  ```
  ipconfig /all
  ```
<p align="left">
  <img src="/lab12-home-network/screenshots/Screenshot1-1.png" width="700">
</p>


* Check the **IP address**, **subnet mask**, and **default gateway**.
* Write down the settings for each PC to find the wrong one.

### Part 2: Fix Configuration Errors

* Select the PC with the wrong configuration.
* Go to **Desktop > IP Configuration** and fix the settings.

<p align="left">
  <img src="/lab12-home-network/screenshots/Screenshot2-1.png" width="700">
</p>

