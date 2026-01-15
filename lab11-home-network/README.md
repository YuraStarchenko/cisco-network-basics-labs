# Packet Tracer – Using Telnet and SSH

<p align="left">
  <img src="/lab11-home-network/screenshots/Screenshot1.png" width="700">
</p>

## Addressing Table

<p align="left">
  <img src="/lab11-home-network/screenshots/Screenshot1-1.png" width="700">
</p>

## Objectives

* Create a remote session with a router using Telnet and SSH
* Check connectivity
* Access a remote device

## Instructions

### Part 1: Check Connection

1. **Check PC IP address**

   * Go to **Desktop > Command Prompt** on the PC.
   * Make sure the PC got an IP address from DHCP.

   **Question:**
   What command did you use to check the DHCP IP address?
   - ``` ftp> ipconfig ```

<p align="left">
  <img src="/lab11-home-network/screenshots/Screenshot1-2.png" width="500">
</p>

2. **Ping HQ Router**

   * Use the IP from the addressing table to ping the HQ router.

<p align="left">
  <img src="/lab11-home-network/screenshots/Screenshot2-1.png" width="500">
</p>


### Part 2: Access Remote Device



1. **Telnet to HQ**

   * Enter:

     ```
     telnet 64.100.1.1
     ```

   **Question:**
   Did the command work? What was the result?
   - ```
   Ні.
   C:\> telnet 64.100.1.1
        Trying 64.100.1.1 ...Open

        [Connection to 64.100.1.1 closed by foreign host] ```

<p align="left">
  <img src="/lab11-home-network/screenshots/Screenshot2-2.png" width="500">
</p>

2. **SSH to HQ**

   * Telnet may be disabled. Use SSH instead:

     ```
     ssh -l admin 64.100.1.1
     ```

     Enter password: `class`

<p align="left">
  <img src="/lab11-home-network/screenshots/Screenshot2-3.png" width="500">
</p>


   **Question:**
   What appears after you successfully log in via SSH?
   - HQ#