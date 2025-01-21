# Transmission QPKG for QNAP

## What It Is

This is a QPKG package designed to simplify the installation of **Transmission** on QNAP NAS devices. Transmission is a lightweight, open-source BitTorrent client known for its speed and ease of use. This QPKG leverages QNAP's **Container Station** and the official Transmission Docker image linuxserver/transmission:4.0.6 for seamless deployment. It is built using QNAP's **QDK Kit**, ensuring compatibility with QNAP systems.

---

## What It Needs

To use this QPKG, you will need:

- A QNAP NAS with **Container Station** installed and configured.
- App Store settings adjusted to allow unsigned applications. This QPKG is unsigned, as it was created independently. To ensure safety, download the QPKG from a trusted source, and you can always review the source code provided on GitHub for transparency.

---

## How to Install

### Step 1: Enable Unsigned Package Installation

Since this QPKG is unsigned, you'll need to allow the installation of unsigned applications:

1. Open your QNAP **App Center**.
2. Navigate to **Settings** > **General**.
3. Enable the option **Allow installation of applications without valid signatures**.

### Step 2: Install the QPKG

1. Download the Transmission QPKG from this repository 
2. Open the App Center on your QNAP device and click **Install Manually**.
3. Select the downloaded QPKG file and follow the on-screen instructions to complete the installation.

---

## Configuration and Initial Run

- On the first run, Transmission will be set up automatically. The default configuration files and settings will be stored in a designated folder within your QNAP shares.
- To access Transmission:
  1. Open a web browser and navigate to:  
     `http://<your-qnap-ip>:9091`  
     Replace `<your-qnap-ip>` with the IP address of your QNAP device (e.g., `192.168.1.100`).
  2. The default username is `qnap_transmission` and the password is `transmission_password`.
  3. We mount ALL your shared folders from QNAP to /mnt directory of transmission container. So its very easy to access the webinterface and specify your download directory. 


## Managing Downloads

Once Transmission is running, you can add torrents via:

1. **Web Interface**:
   - Upload `.torrent` files or paste magnet links directly into the web interface.
2. **Watch Folder**:
   - Place `.torrent` files into the designated "watch folder," and Transmission will start downloading them automatically.
   - The watch folder location can be configured in the settings.

---

## Credits

- Built with QNAP's **QDK Kit**.
- Powered by the official Transmission Docker image: [linuxserver/transmission](https://hub.docker.com/r/linuxserver/transmission).

---

Enjoy seamless torrent downloading with Transmission on your QNAP NAS!
