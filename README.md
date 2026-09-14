
![Banner](img/banner.png?raw=true)
=====

# GRID0 Hub

> **WIP Notice**: Official hub for GRID0 network routing and client setup.

GRID0 is a virtual overlay network bridging all three Switch ecosystems into the same LAN lobby:
* **Emulators** (PC)
* **CFW** (Atmosphère, Modded Switch 1)
* **OFW** (Stock Hardware, Unmodded Switch 1 and Switch 2)

---

## Quick Connection Matrix

| Ecosystem | Platform / Environment | Core Tool | Connection Method |
| :--- | :--- | :--- | :--- |
| **Emulator** | PC / Steam Deck (Ryujinx, Suyu) | **ZeroTier One** | Desktop client binds directly to emulator network adapter. |
| **CFW** | Modded Switch (Atmosphère) | **sys-zerotier** | On-device background sysmodule. No host PC required. |
| **OFW** | Unmodded Stock Switch or Switch 2 | **grid0-overlay** | PC companion application bridges Switch Wi-Fi traffic. |

---

## Setup Guides

### 1. Emulator Setup (PC, Windows)

If you play on an emulator you just need the native ZeroTier client.

1. Download and install **[ZeroTier One](https://www.zerotier.com/download/)**.
2. Launch ZeroTier, right-click the tray icon, select **Join New Network**, and enter:
   `8bd5124fd68185ec` [PLEASE NOTE THAT YOU MAY ENTER ANY ADDRESS YOU LIKE, THIS ADDRESS IS SIMPLY FOR CONNECTING TO GRID0]
3. Open your emulator settings (e.g. Ryujinx):
   * Go to **Settings → Network**.
   * Set **Mode** to `Disabled`.
   * Enable **Guest Internet Access/LAN Mode**
   * Remember to click **Apply** and/or **OK**.

---

### 2. Modded Switch 

Runs directly on the console as a background sysmodule. No PC or phone required while playing.

1. Download the latest release from the **[sys-zerotier repository](https://github.com/redluigi323/sys-zerotier/)**.
2. Extract the archive to the root of your SD card.
4. Reboot into Atmosphère and verify connection status using the Tesla overlay menu.

