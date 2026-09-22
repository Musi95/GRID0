![Banner](img/banner.png?raw=true)
=====

![License](https://img.shields.io/badge/License-GPLv2-blue.svg)
[![Chat on Discord](https://img.shields.io/badge/Discord-5865f2?logo=discord&logoColor=white)](https://discordapp.com/invite/splatfest)

# Welcome to GRID0

> **WIP Notice**: Official hub for GRID0 network routing and client setup. GRID0 is a virtual overlay network bridging all three Switch ecosystems into the same LAN lobby:
* **Emulators** (PC)
* **CFW** (Atmosphère, Modded Switch 1)
* **OFW** (Stock Hardware, Unmodded Switch 1 and Switch 2)

---

## Quick Connection Matrix

| Ecosystem | Platform / Environment | Core Tool | Connection Method |
| :--- | :--- | :--- | :--- |
| **Emulator** | PC / Steam Deck (Ryujinx, Astris, Eden, etc.) | **ZeroTier One** | Desktop client binds directly to emulator network adapter. |
| **CFW** | Modded Switch (Atmosphère) | **sys-GRID0** | On-device background sysmodule. No host PC required. |
| **OFW** | Unmodded Stock Switch or Switch 2 | **GRID0-relay** | PC companion application bridges Switch Wi-Fi traffic. |

---

## Setup Guides

### 1. Emulator Setup (PC, Windows)

If you play on an emulator you just need the native ZeroTier client.

1. Download and install **[ZeroTier One](https://www.zerotier.com/download/)**.
2. Launch ZeroTier, right-click the tray icon, select **Join New Network**, and enter:
   `8bd5124fd68185ec`
3. Open your emulator settings (e.g. Ryujinx):
   * Go to **Settings → Network**.
   * Set **Mode** to `Disabled`.
   * Enable **Guest Internet Access/LAN Mode**
   * Remember to click **Apply** and/or **OK**.

---

### 2. Modded Switch 

Runs directly on the console as a background sysmodule. No PC or phone required while playing.

1. Download the latest release from the **[sys-GRID0](https://github.com/redluigi323/sys-GRID0/)**.
2. Extract the archive to the root of your SD card.
4. Reboot into Atmosphère and verify connection status using the Tesla (or Ultrahand) overlay menu.

---

### 3. Stock Switch and Switch 2 Setup (OFW)

Stock consoles cannot execute background custom modules. `grid0-relay` runs on a PC connected to the same home network, capturing and translating LAN-Play packets automatically.

1. Download and open `GRID0Relay.exe` from the **[GRID0-relay](https://github.com/redluigi323/grid0-relay)**.
2. `GRID0Relay` will automatically install ZeroTier One and npcap.  
<small><details><summary>For certainty:</summary>Make sure they are installed (it should say ZeroTier One and npcap are installed in the `GRID0Relay` settings).</details></small>
4. `GRID0Relay` will automatically launch ZeroTier and connect to the GRID0 network.  
<small><details><summary>For certainty:</summary>Windows: Click the Up arrow at the bottom right of your screen and right-click the ZeroTier tray icon, make sure there is a check mark beside "`GRID0Relay` GRID0.</details></small>
5. `GRID0Relay` will automatically select the correct ZeroTier adapter.
<small><details><summary>For certainty:</summary>In `GRID0Relay`, open **Settings**, the relay will automatically connect to the presumed ZeroTier connection, but make sure the ZeroTier connection selected looks like the correct one (should be named something similar to ZeroTier).</details></small>
7. Go back to the **Play** section of `GRID0Relay` and notice the Switch IP settings it provides you.
8. On your Switch or Switch 2, enter **Network Settings**, **Change Settings** on the same network your PC is connected to, and enter the provided IP setting. (Primary DNS can be set to ***8.8.8.8** and Secondary DNS can be left blank).
9. Make sure to save and connect to the network.
