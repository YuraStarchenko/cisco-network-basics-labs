# Packet Tracer – NAT Check on a Wireless Router

## Goals

- Check NAT on a wireless router
- Connect four PCs using DHCP
- Check traffic using NAT

## Part 1: External Network

1. Add 1 PC and connect it to the router.
2. On PC: Desktop → IP Configuration → DHCP
3. Write down default gateway IP.
4. Open browser → type gateway IP → login: admin/admin
5. Status → Internet → check IP

<p align="left">
   <img src="/lab04-home-network/screenshots/Screenshot1-1.png" width="700">
   <img src="/lab04-home-network/screenshots/Screenshot1-2.png" width="700">
   <img src="/lab04-home-network/screenshots/Screenshot1-3.png" width="700">
</p>

## Part 2: Internal Network

1. Status → Local Network → check internal IP
2. Check DHCP range

<p align="left">
   <img src="/lab04-home-network/screenshots/Screenshot2-1.png" width="700">
</p>

## Part 3: Connect More PCs

1. Add 3 more PCs → connect to router
2. On each PC: Desktop → IP Configuration → DHCP
3. Command Prompt → `ipconfig /all`

<p align="left">
   <img src="/lab04-home-network/screenshots/Screenshot3-1.png" width="700">
   <img src="/lab04-home-network/screenshots/Screenshot3-2.png" width="700">
</p>

## Part 4: NAT Simulation

1. Switch to Simulation mode
2. Simulation Panel → Show All/None → Edit Filters → check TCP & HTTP
3. Click envelope icon → Create Complex PDU
4. Set source: PC, destination: ciscolearn.nat.com
5. PDU Settings:
   - Application: HTTP
   - Source port: 1000
   - Simulation: Periodic, Interval 120s
6. Click Create PDU → Play animation

<p align="left">
   <img src="/lab04-home-network/screenshots/Screenshot4-1.png" width="700">
   <img src="/lab04-home-network/screenshots/Screenshot4-2.png" width="700">
</p>

## Part 5: Check Packets

1. Double-click a packet in Simulation Panel
2. Check Inbound and Outbound headers
3. Observe SRC IP change (NAT works!)
4. Repeat for other packets
5. Click Check Results when done

<p align="left">
   <img src="/lab04-home-network/screenshots/Screenshot5-1.png" width="700">
   <img src="/lab04-home-network/screenshots/Screenshot5-2.png" width="700">
</p>

## Notes

- Private IPs cannot go to the Internet directly.
- NAT changes source IP for Internet access.
