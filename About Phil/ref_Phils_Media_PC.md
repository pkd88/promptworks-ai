

# **1.0 Media-PC Technical Specification Sheet**

This document provides a comprehensive technical inventory and configuration profile for the system designated as Media-PC. It is intended for use by system administrators and automated retrieval systems to verify hardware, software, and network environments.

## **2.0 System Overview**

This section details the core hardware components and the base operating system environment for the Media-PC. It serves as the primary reference for the system's processing power, memory capacity, and installation history.

| Category | Component / Detail |
| :---- | :---- |
| System Name | Media-PC |
| Processor (CPU) | 11th Gen Intel(R) Core(TM) i9-11900H @ 2.50GHz (8 Cores, 16 Threads) |
| Memory (RAM) | 64.0 GB DDR4 @ 3200 MT/s |
| Graphics (GPU) | Intel(R) UHD Graphics (32 GB shared VRAM) |
| Primary Monitor | Acer SA241Y |
| Operating System | Windows 11 Pro (Version 25H2, Build 26200.8037) |
| Installation Date | November 10, 2024 |

## **3.0 Storage Configuration**

This section outlines the local, external, and network-attached storage architecture of the system. Use this information to locate system files, service data, and mapped media libraries.

| Drive Letter | Label | Capacity | Hardware Type |
| :---- | :---- | :---- | :---- |
| C: | System | 500 GB | NVMe SSD |
| Z: | ServiceDrive | 14 TB | External USB Drive |
| B: | Books | Network | Synology NAS Mapped Drive |
| E: | Exercise | Network | Synology NAS Mapped Drive |
| M: | Movies | Network | Synology NAS Mapped Drive |
| T: | Television | Network | Synology NAS Mapped Drive |

## **4.0 Network & Peripherals**

This section covers the connectivity hardware, virtual private networking, and remote access tools configured on the system. It also includes information regarding network-connected peripheral devices.

- **Wireless:** Realtek 8852BE WiFi 6  
- **Ethernet:** Realtek PCIe GbE Family Controller  
- **VPN:** ExpressVPN (TAP, TUN, and OpenVPN drivers installed)  
- **Remote Access:** Tailscale, Chrome Remote Desktop, Synology Assistant  
- **Printer:** Brother (Network via WSD)

## **5.0 Installed Software Stack**

This section provides an exhaustive list of the software applications installed on the system, categorized by their primary function. This includes media automation, development environments, and security tools.

### **5.1 Media & Automation**

This subsection lists the tools used for media server management, content tracking, and automated downloading.

- **Server:** Emby Server  
- **Trackers:** Sonarr (TV), Radarr (Movies), Readarr (Books), Prowlarr (Indexers)  
- **Downloaders:** SABnzbd (Usenet), qBittorrent (Torrents)  
- **Tools:** FileBot (Renamer), Calibre (E-books)

### **5.2 Artificial Intelligence & Development**

This subsection details the local AI orchestration tools, database versions, and programming environments available on the system.

- **AI Orchestration:** AnythingLLM, Ollama  
- **Database:** PostgreSQL 18  
- **Environments:** Python (3.12 & 3.13), Ubuntu (WSL)

### **5.3 Cloud & File Management**

This subsection identifies the synchronization clients and transfer tools used for managing data across cloud and local platforms.

- **Sync Clients:** Synology Drive, Google Drive, OneDrive  
- **Transfer Tools:** rclone, Cyberduck  
- **Security:** Bitwarden

## **6.0 System Folders for Backups**

This section identifies the specific directory paths that must be backed up to preserve application settings. Regularly saving these folders to cloud storage ensures that configurations for the automation stack are not lost.

Save the following folders to your cloud storage to preserve all application settings:

- `C:\ProgramData\Sonarr`  
- `C:\ProgramData\Radarr`  
- `C:\ProgramData\Prowlarr`  
- `C:\ProgramData\Readarr`

Would you like a list of the specific network IP addresses for these devices?

## **7.0 References**

This section is reserved for external links and documentation sources referenced in the text.

1. \[No URLs found in source document\]

END OF INSTRUCTIONS

Functional Intent: Technical inventory of Media-PC hardware and software.

Authority Level: Level 3 (Standard)

Linked Entities: ref\_Phil's Media PC, ref\_Markdown\_RAG\_Standard

