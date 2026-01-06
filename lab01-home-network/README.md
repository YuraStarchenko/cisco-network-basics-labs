# Lab 01 — Home Network Setup (Packet Tracer)

## Description
This lab shows how to create a simple home network in Cisco Packet Tracer.
The network uses wired and wireless connections with basic security.

## Part 1: Device Connections

This screenshot shows the home network setup in Cisco Packet Tracer.
Coaxial cable connects Internet and TV services
Cable Splitter separates Internet and TV signals
Cable Modem is connected to the Home Wireless Router
Two PCs are connected with Ethernet cables
The router provides Internet access to all devices

Result:
All wired devices are connected and the network has Internet access.

![Home Network Setup](screenshots/Screenshot1.png)


## Part 2: Setup Home Wireless Router

Most home wireless routers use a GUI (Graphical User Interface) in a web browser. In this part, you access the router from the Office PC and set up the home network.

## Step 1: Access the Router GUI

On Office PC → Desktop → IP Configuration, click DHCP.

![Home Network Setup](screenshots/Screenshot2.png)

The PC gets an IP from the router automatically (IP starts with 192).

Write down the Default Gateway (this is the router’s IP).

Open Web Browser, enter the router IP, and log in:
Username: admin, Password: admin.
![Home Network Setup](screenshots/Screenshot3.png)

Default passwords should be changed on real devices.

## Step 2: Set Basic Settings
Go to Setup → Network Setup → Maximum Number of Users and set 10.

![Home Network Setup](screenshots/Screenshot4.png)
Save settings.

Go to Administration and change password to MyPassword1!.
Log in again with the new password.

![Home Network Setup](screenshots/Screenshot5.png)
![Home Network Setup](screenshots/Screenshot7.png)
![Home Network Setup](screenshots/Screenshot12.png)

## Step 3: Set Wireless Network

Go to Wireless → Enable 2.4 GHz.
Change SSID to MyHome.

![Home Network Setup](screenshots/Screenshot6.png)

Go to Wireless Security → WPA2 Personal.
Set Passphrase: MyPassPhrase1!

![Home Network Setup](screenshots/Screenshot8.png)
Save settings.
Close the browser.

## Part 3: Set IP and Test Connection
Now the router is ready. In this part, we set IP addresses for PCs and check internet connection.

## Step 1: Connect Laptop to Wi-Fi
On Laptop → Desktop → PC Wireless → Connect, find the network MyHome.

![Home Network Setup](screenshots/Screenshot9.png)

Enter Pre-shared Key: MyPassPhrase1! and click Connect.
Check Link Information → “You have successfully connected to the access point.”

![Home Network Setup](screenshots/Screenshot10.png)

Open Web Browser and go to skillsforall.srv to test internet.

![Home Network Setup](screenshots/Screenshot11.png)

If IP is not starting with 192, click Fast Forward Time.

## Step 2: Test Office PC
On Office PC → Desktop → Web Browser, go to skillsforall.srv.
This confirms that Office PC is connected to the internet.

![Home Network Setup](screenshots/Screenshot13.png)

## Step 3: Setup Bedroom PC
On Bedroom PC → IP Configuration, select DHCP.
Open Web Browser and go to skillsforall.srv.
Check that Bedroom PC can access the internet.

![Home Network Setup](screenshots/Screenshot14.png)
![Home Network Setup](screenshots/Screenshot15.png)

All devices now have internet access. Lab complete!
Your friend Natsumi thanks you with lunch.
