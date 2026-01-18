# Lab 02 — Home Network Setup

## Packet Tracer — Connecting to a Web Server

## Description
This lab demonstrates how to test connectivity to a web server in **Cisco Packet Tracer**.  
You will observe how packets are sent over the Internet using IP addresses.

---

## Goals and Tasks

- Observe packet transmission using IP addressing  
- Test connectivity using **ping**
- Access a web server using a **web browser**

---

## Part 1: Test Connection to the Web Server

In this part, you verify connectivity to the web server using the `ping` command.

### Step 1: Use Command Prompt

a. Open the command line on the source host (**PC0**).  
b. Go to `Desktop` → `Command Prompt`.  
c. Test the connection to the web server by entering the following command:

```bash
ping 172.33.100.50
```
Testing the connection to the web server using ping.

<p align="left">
  <a href="/lab02-home-network/screenshots/Screenshot1.png">
    <img src="/lab02-home-network/screenshots/Screenshot1.png" width="500">
  </a>
</p>

### Result

The reply confirms that the client is successfully connected to the destination web server.
The first reply may take longer because devices are initializing and ARP is resolving MAC addresses.

### Part 2: Connect to the Web Server Using a Web Client

In this part, you access the web server using a web browser.

### Step 2: Use Web Browser

a. On PC0 → Desktop, open Web Browser.
b. Enter 172.33.100.50 in the URL bar and click Go.

The web page opens successfully using the server IP address.

Testing the connection to the web server using Web Browser.

<p align="left">
  <a href="/lab02-home-network/screenshots/Screenshot2.png">
    <img src="/lab02-home-network/screenshots/Screenshot2.png" width="500">
  </a>
</p>

✅ Lab Complete
- The client can successfully reach the web server using both:
- ICMP (ping)
- HTTP (web browser)
- Lab complete! 🎉
