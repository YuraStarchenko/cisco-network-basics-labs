# Packet Tracer – Traffic Flow in a Routed Network

## Scenario

You work for a company that prepares a new network design for XYZ LLC. XYZ is a
growing startup. The current network uses one IPv4 subnet for all departments.
This causes delays and low performance.

Your task is to show how routing between departments can improve network
efficiency and scalability.

## Instructions

### Part 1: Traffic Flow in a Non-Routed LAN

The XYZ network has about 150 devices in one LAN and one IPv4 subnet. All
departments are in the same network. The edge router only connects the LAN to
the ISP.

Use Simulation Mode in Packet Tracer to observe traffic behavior.

### Step 1: Clear ARP Cache on Sales 1

- Check the IP address of Sales 1
- Open Desktop > Command Prompt
- Run arp -a
- If entries exist, delete them with arp -d

![Home Network Setup](/lab06-home-network/screenshots/Screenshot1-1.png)

### Step 2: Explore Network Traffic

- Switch to Simulation Mode
- From Sales 2, ping the IP address of Sales 1
- Use Capture then Forward to follow the PDU
- Open the PDU to view frame and packet details

![Home Network Setup](/lab06-home-network/screenshots/Screenshot1-2.png)
![Home Network Setup](/lab06-home-network/screenshots/Screenshot1-3.png)

Questions:

- What are the source and destination MAC and IP addresses?
- Source MAC: Sales 1
- Destination MAC: FFFF.FFFF.FFFF (broadcast)
- Source IP: Sales 1
- Destination IP: Sales 2

- Why is the destination MAC address a broadcast?
- The ARP cache is empty, so the host sends an ARP request to get the
  destination MAC address.

- Which devices process ARP requests?
- All hosts and the router interface.

- How does this affect network performance?
- If the ARP cache is empty, an ARP broadcast is sent and processed by all
  hosts.
- In large networks, frequent ARP broadcasts reduce network performance.

- What type of PDU is created after ARP?
- This is the first ICMP echo request packet sent by Sales 2 using the ping
  command.

Return to Realtime Mode after finishing.

## Part 2: Reconfigure Network for Inter-VLAN Routing

In this part, you will see the benefits of routing between department networks.
Each switch is now connected directly to the Edge router. Nodes get new IPs from
two new subnets.

### Step 1: Change Device Connections

Connect Accounting, Finance, and Sales switches to the Edge router using
GigabitEthernet ports.

![Home Network Setup](/lab06-home-network/screenshots/Screenshot2-1.png)

### Step 2: Configure Nodes with New IPs

Each Edge router interface has its own IPv4 subnet. Nodes in Finance and Sales
need new IPs. On each device in Finance and Sales, run: ipconfig /renew

![Home Network Setup](/lab06-home-network/screenshots/Screenshot2-2.png)

to get a new IP from the router’s DHCP.

Questions:

- What is the subnet for Finance?
- 192.168.2.0/24

- What is the subnet for Sales?
- 192.168.3.0/24

## Part 3: Traffic Flow in a Routed Network

### Step 1: Ping Sales 1 from Sales 2

On Sales 2, clear the ARP cache if needed.

Switch to Simulation Mode.

Ping Sales 1. Use Capture then Forward to follow PDUs. Note how ARP messages
travel through the routed network.

![Home Network Setup](/lab06-home-network/screenshots/Screenshot3-1.png)

Question:

- Which devices now receive the ARP broadcast?
- Only Sales 1 and the router interface for the Sales network handle the PDU.

### Step 2: Ping Other Hosts

Ping other nodes and the Internet server. Observe the ARP PDU flow.

![Home Network Setup](/lab06-home-network/screenshots/Screenshot3-2.png)
![Home Network Setup](/lab06-home-network/screenshots/Screenshot3-3.png)

Question:

- What is the benefit of using multiple networks or subnets in a company?

- The main benefit of using multiple IP networks is keeping traffic in the right
  network parts, without affecting other parts
