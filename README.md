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
| **OFW** | Unmodded Stock Switch | **grid0-overlay** | PC companion application bridges Switch Wi-Fi traffic. |

---
