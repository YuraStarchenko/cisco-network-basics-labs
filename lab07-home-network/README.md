# Packet Tracer – Creating a LAN

## Address Table

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot1-1.png" width="700">
</p>


### Objectives

- Connect network devices and hosts

- Set IPv4 addresses on devices

- Test device connections

- Use network commands to check host info

### Scenario

A new office opens, and you need to set up a LAN.
Devices are ready, but you must connect them to hosts, configure IPv4 addresses, and verify access to local and remote resources.

## Instructions

### Part 1: Connect Devices

1. Power on devices

- Open Physical tab on each device
- Turn on the power (green light shows device is on)

2. Connect hosts

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot1-2.png" width="700">
</p>

- Use the Connections Table
- Connect devices with copper straight-through Ethernet cables
- Internet connects to office router via the cloud menu
- Connect PCs and printer to the office switch
- After a short delay, green link lights should appear


<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot1-3.png" width="600">
  <img src="/lab07-home-network/screenshots/Screenshot1-4.png" width="400">
</p>

Note:
- Interfaces with G = GigabitEthernet
- Interfaces with F = FastEthernet


## Part 2: Configure Devices with IPv4

### Step 1: Configure Hosts

1. Admin PC and Manager PC get IP from DHCP (office router).
- Open Desktop > IP Configuration
- Set to dynamic IP

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot2-1.png" width="700">
</p>

2. Printers and servers use static IP so other devices can always reach them.
- Open Config > FastEthernet0 on the printer
- Enter IP info from the Address Table
- PCs in the same network have similar IPs, same subnet mask and default gateway.

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot2-2.png" width="500">
</p>

### Questions:

1. Why are IP addresses different but subnet masks and gateways the same?
- Answers may vary. Each device needs a unique ID.
- The IPv4 address identifies the host.
- The default gateway connects to devices outside the local network.

2. A printer does not need a default gateway. If you set one, what value would it use? How can you find it from other devices?
- The default gateway can be found from the PCs’ DHCP settings or the IP of the office router’s LAN interface.


## Part 3: Configure Devices and Test Connections

### Step 1: Test PC Connections

1. Check IP settings on each PC.
- They get dynamic IPs in 192.168.1.0/24
- They also get default gateway and DNS

2. On Admin and Manager PCs, ping the printer.
- Successful replies show devices are on, connected, and correctly addressed

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot3-1.png" width="600">
</p>

### Step 2: Test Internet Access

- Open a browser on each PC
= Access the Internet server by IP and by URL

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot3-2.png" width="500">
</p>

### Question:

1. If you can reach the server by IP but not URL, what is the possible reason?
- Since DNS converts URLs to IPs, the DNS server is likely unavailable.
This can happen if the network is down or the DNS address on the host is missing or wrong.

## Part 4: Use Network Commands to Check Host Info

### Step 1: Use ipconfig

- Shows IP, subnet mask, gateway, and more on the PC

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot4-1.png" width="600">
</p>

### Question:

1. Run ipconfig and ipconfig /all. What extra information appears with /all?
- The ipconfig /all command shows the NIC’s MAC address and DHCP and DNS server info.
In Windows, it shows more details. Run it on a PC to see all information.

### Step 2: Use tracert

Shows the route from the PC to a destination using ICMP

* Tasks:

Run tracert <webserver URL> from a PC

<p align="left">
  <img src="/lab07-home-network/screenshots/Screenshot4-2.png" width="700">
</p>

### Questions:

1. How many routers are on the path? How are they identified?
- Two. They are identified by the IP addresses of their router interfaces.

2. Where is the second router located?
- In the Internet cloud.











