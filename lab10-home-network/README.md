## Packet Tracer – Using FTP Services

<p align="left">
  <img src="/lab10-home-network/screenshots/Screenshot1.png" width="500">
</p>

### Addressing Table

<p align="left">
  <img src="/lab10-home-network/screenshots/Screenshot1-1.png" width="700">
</p>

### Objectives

* Upload a file to an FTP server
* Download a file from an FTP server

### Background

FTP (File Transfer Protocol) is used to transfer files between a client and a server.
FTP uses **port 21** for commands and **port 20** for data transfer.

---

## Part 1: Upload a File to the FTP Server

1. On **PC-A**, open **Desktop → Command Prompt**.
2. Use `dir` to find **sampleFile.txt** on drive C:.
3. Connect to the FTP server:

   ```
   ftp 209.165.200.226
   ```
4. Login:

   * Username: `student`
   * Password: `class`
5. Check server files with:

   ```
   dir
   ```
6. Upload the file:

   ```
   put sampleFile.txt
   ```
7. Use `dir` again to confirm the upload.

<p align="left">
  <img src="/lab10-home-network/screenshots/Screenshot1-2.png" width="300">
  <img src="/lab10-home-network/screenshots/Screenshot1-3.png" width="300">
  <img src="/lab10-home-network/screenshots/Screenshot1-4.png" width="300">
  <img src="/lab10-home-network/screenshots/Screenshot1-5.png" width="300">
</p>


---

## Part 2: Download a File from the FTP Server

1. Rename the file on the server:

   ```
   rename sampleFile.txt sampleFile_FTP.txt
   ```
2. Download the file:

   ```
   get sampleFile_FTP.txt
   ```
3. Exit FTP:

   ```
   quit
   ```

<p align="left">
  <img src="/lab10-home-network/screenshots/Screenshot2-1.png" width="300">
  <img src="/lab10-home-network/screenshots/Screenshot2-2.png" width="300">
</p>


---

## Part 3: Delete the File from the FTP Server

1. Connect to the FTP server again.
2. Delete the file:

   ```
   delete sampleFile_FTP.txt
   ```
3. Exit FTP with `quit`.

<p align="left">
  <img src="/lab10-home-network/screenshots/Screenshot2-3.png" width="400">
</p>

---

### Question

**Which command is used to delete a file from the FTP server?**
**Answer:** `delete sampleFile_FTP.txt`