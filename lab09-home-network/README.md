## Packet Tracer – Tracing Web Requests

### Objective

View client and server traffic sent from a PC to a web server when accessing web services.

---

## Part 1: Test Web Server Connectivity

1. Open **External Client** → **Desktop** → **Command Prompt**.
2. Use the ping command:

```
ping ciscolearn.web.com
```

<p align="left">
  <img src="/lab09-home-network/screenshots/Screenshot1-1.png" width="300">
</p>

3. Note the IP address returned by DNS. Network traffic uses source and destination IP addresses.
4. Close Command Prompt, keep External Client open.

---

## Part 2: Connect to the Web Server

1. Open **Web Browser** on External Client.
2. Enter:

```
ciscolearn.web.com
```

<p align="left">
  <img src="/lab09-home-network/screenshots/Screenshot2-1.png" width="400">
</p>

3. Read the web page and keep it open.
4. Minimize External Client.

---

## Part 3: View HTML Code

1. Click **ciscolearn.web.com server** in the topology.
2. Open **Services > HTTP** and click **Edit** next to `index.html`.
3. Compare the HTML code with the page shown in the browser.
4. Close all windows.

<p align="left">
  <img src="/lab09-home-network/screenshots/Screenshot3-1.png" width="500">
  <img src="/lab09-home-network/screenshots/Screenshot3-2.png" width="300">
  <img src="/lab09-home-network/screenshots/Screenshot3-3.png" width="500">
</p>

---

## Part 4: Analyze Network Traffic

1. Switch to **Simulation mode**.
2. Open **Simulation Panel** and enable only **TCP** and **HTTP** filters.
3. Create a **Complex PDU**:

   * Source: External Client
   * Application: HTTP
   * Destination: ciscolearn.web.com
   * Source Port: 1000
   * Interval: 120 seconds
4. Click **Play** to observe traffic flow.

<p align="left">
  <img src="/lab09-home-network/screenshots/Screenshot4-1.png" width="400">
  <img src="/lab09-home-network/screenshots/Screenshot4-2.png" width="300">
  <img src="/lab09-home-network/screenshots/Screenshot4-3.png" width="500">
</p>

**Note:** HTTP uses TCP, so connection setup and acknowledgements increase traffic volume.
