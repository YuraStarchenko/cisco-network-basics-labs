## Packet Tracer – Client Interaction

### Objectives

* Observe client–server interaction between a PC and a server

### Scenario

Clients (PCs) send service requests to servers.
In this lab, a **PC connects directly to a server** that provides **DNS** and **HTTP** services.
You will observe traffic when a web page is requested, how the URL is resolved to an IP, and how the web page is 
delivered.

### Instructions

#### Part 1: Switch to Simulation Mode

* Click **Simulation Mode** in the bottom-right corner

<p align="left">
  <img src="/lab08-home-network/screenshots/Screenshot1-1.png" width="400">
</p>

#### Part 2: Set Event List Filters

* Clear all filters (**Show All/None**)
* Enable **DNS** (IPv4 tab) and **HTTP** (Misc tab)

<p align="left">
  <img src="/lab08-home-network/screenshots/Screenshot2-1.png" width="400">
</p>

#### Part 3: Request a Web Page

* Open **PC > Desktop > Web Browser**
* Enter `www.example.com` and click **Go**
* Minimize the PC window

<p align="left">
  <img src="/lab08-home-network/screenshots/Screenshot3-1.png" width="700">
</p>

#### Part 4: Run the Simulation

* Click **Play** in the Simulation Panel
* Observe DNS and HTTP events in the Event List
* Use **View Previous Event** if the buffer is full

<p align="left">
  <img src="/lab08-home-network/screenshots/Screenshot4-1.png" width="700">
</p>

#### Part 5: Open a PDU

* Restore the PC window and confirm the web page loads
* In the Event List, click the **colored box** of the first event to open **PDU Information**

<p align="left">
  <img src="/lab08-home-network/screenshots/Screenshot5-1.png" width="400">
</p>

#### Part 6: Review PDU Details

* Use **Next Layer >>** to view OSI layers
* Review other PDUs to understand the full communication process

<p align="left">
  <img src="/lab08-home-network/screenshots/Screenshot6-1.png" width="250">
  <img src="/lab08-home-network/screenshots/Screenshot6-2.png" width="250">
  <img src="/lab08-home-network/screenshots/Screenshot6-3.png" width="250">
  <img src="/lab08-home-network/screenshots/Screenshot6-4.png" width="250">
  <img src="/lab08-home-network/screenshots/Screenshot6-5.png" width="250">
  <img src="/lab08-home-network/screenshots/Screenshot6-6.png" width="250">
  <img src="/lab08-home-network/screenshots/Screenshot6-7.png" width="250">
</p>
