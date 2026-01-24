# Packet Tracer – Using the ping Command

<p align="left">
  <img src="/lab13-home-network/screenshots/Screenshot1.png" width="700">
</p>

## Objectives

- Use the **ping** command to find a PC configuration problem.

## Scenario

A small business owner reports that some users cannot open a website. All PCs
use **static IP addresses**. Use **ping** to find the issue.

## Instructions

### Part 1: Check Connectivity

- On each PC, go to **Desktop > Web Browser**.
- Enter: `www.cisco.pka`
- Find which PCs cannot connect to the web server.

<p align="left">
  <img src="/lab13-home-network/screenshots/Screenshot1-2.png" width="700">
</p>

**Question:** Which PCs cannot connect to the web server?

- `PC2`

### Part 2: Ping from Problem PCs

- On a problem PC, open **Desktop > Command Prompt**.
- Run:

  `ping cisco.com`

  <p align="left">
    <img src="/lab13-home-network/screenshots/Screenshot2-1.png" width="700">
  </p>

**Question:** Did you get a reply? What IP address is shown?

- There was no reply. The IP address was not shown in the message.

### Part 3: Ping from Working PCs

- On a working PC, open **Command Prompt**.
- Run:

  `ping cisco.com`

<p align="left">
  <img src="/lab13-home-network/screenshots/Screenshot3-1.png" width="700">
</p>

**Question:** Did the ping reply? What IP address is returned?

- 192.15.2.10

### Part 4: Ping Server IP from Problem PCs

- On a problem PC, ping the **IP address** of the web server.

If ping works by IP but not by name, this shows a **DNS problem**.

<p align="left">
  <img src="/lab13-home-network/screenshots/Screenshot4-1.png" width="700">
</p>

### Part 5: Compare DNS Settings

- On working PCs, run:

  `ipconfig /all`

- Check DNS server settings.
- Do the same on problem PCs.

<p align="left">
  <img src="/lab13-home-network/screenshots/Screenshot5-1.png" width="500">
  <img src="/lab13-home-network/screenshots/Screenshot5-2.png" width="500">
</p>

**Question:** Are the DNS settings the same?

- No, the DNS settings are different.

### Part 6: Fix the Configuration

- On problem PCs, go to **Desktop > IP Configuration** and fix the settings.
- Open **Web Browser** and connect to `www.cisco.pka` to confirm the issue is
  fixed.

<p align="left">
  <img src="/lab13-home-network/screenshots/Screenshot6-1.png" width="500">
  <img src="/lab13-home-network/screenshots/Screenshot6-2.png" width="500">
</p>
