## Packet Tracer – DHCP on a Wireless Router

## Goals

* Connect 3 PCs to a wireless router
* Change DHCP settings
* Let PCs get IP addresses automatically

## Scenario

A home user wants to connect 3 PCs to a wireless router. All PCs get IP addresses from the router automatically.

## Part 1: Connect the network

1. Add 3 PCs.
2. Connect each PC to the router with a cable.

<p align="left">
  <img src="/lab03-home-network/screenshots/Screenshot1.png" width="700">
</p>

## Part 2: Use default DHCP

1. Click PC0 → Desktop → IP Configuration → DHCP.
2. Open the web browser on PC0.
3. Enter the router IP in the browser. Username: admin, password: admin.
4. Look at default settings. DHCP is ON.

<p align="left">
  <img src="/lab03-home-network/screenshots/Screenshot2.png" width="700">
  <img src="/lab03-home-network/screenshots/Screenshot3.png" width="700">
  <img src="/lab03-home-network/screenshots/Screenshot3-1.png" width="700">
</p>


## Part 3: Change router IP

1. Change router IP to 192.168.5.1.
2. Click Save Settings.
3. Close the browser.
4. On PC0, go to IP Configuration → Static → DHCP to get new IP.
5. Open browser again, enter 192.168.5.1, username: admin, password: admin.


<p align="left">
  <img src="/lab03-home-network/screenshots/Screenshot4.png" width="700">
</p>

## Part 4: Change DHCP range

1. Change start IP to 192.168.5.26.
2. Change max users to 75.
3. Click Save Settings.
4. On PC0, go to IP Configuration → Static → DHCP to get new IP.
5. Open Command Prompt → type ipconfig to see IP.

<p align="left">
  <img src="/lab03-home-network/screenshots/Screenshot5.png" width="700">
  <img src="/lab03-home-network/screenshots/Screenshot6.png" width="700">
  <img src="/lab03-home-network/screenshots/Screenshot7.png" width="700">
</p>

## Part 5: Enable DHCP on PC1 and PC2

1. Click PC1 → Desktop → IP Configuration → DHCP.
2. Repeat for PC2.

<p align="left">
  <img src="/lab03-home-network/screenshots/Screenshot8.png" width="700">
  <img src="/lab03-home-network/screenshots/Screenshot9.png" width="700">
</p>

## Part 6: Test the network

1. On PC2 → Desktop → Command Prompt → ipconfig.
2. Type ping 192.168.5.1 (router).
3. Type ping 192.168.5.126 (PC0).
4. Type ping 192.168.5.127 (PC1).
5. All pings should work.

<p align="left">
  <img src="/lab03-home-network/screenshots/Screenshot10.png" width="700">
</p>