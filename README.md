<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Networking Basics](#networking-basics)
  - [Course Purpose](#course-purpose)
  - [Repository Structure](#repository-structure)
    - [What's Included](#whats-included)
  - [Learning Outcomes](#learning-outcomes)
  - [Prerequisites](#prerequisites)
  - [Getting Started](#getting-started)
    - [Option 1: Use with Obsidian (Recommended)](#option-1-use-with-obsidian-recommended)
    - [Option 2: Browse on GitHub](#option-2-browse-on-github)
  - [Course Modules](#course-modules)
  - [Hands-On Labs](#hands-on-labs)
  - [Anki Flashcards](#anki-flashcards)
    - [What's Included](#whats-included-1)
    - [Getting Started with Anki](#getting-started-with-anki)
      - [1. Download Anki](#1-download-anki)
      - [2. Import Flashcard Decks](#2-import-flashcard-decks)
      - [3. Start Studying](#3-start-studying)
      - [4. Sync Across Devices (Optional)](#4-sync-across-devices-optional)
    - [Study Tips](#study-tips)
    - [Flashcard Coverage by Module](#flashcard-coverage-by-module)
  - [How to Use This Repository](#how-to-use-this-repository)
  - [Features](#features)
  - [Learning Resources](#learning-resources)
  - [System Requirements](#system-requirements)
  - [Contributing](#contributing)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)
  - [Next Steps](#next-steps)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Networking Basics

A comprehensive Obsidian vault containing structured notes, practical labs, and reference materials for Cisco's Networking Basics course. This repository provides an organized, hands-on approach to mastering fundamental networking concepts essential for IT professionals, cybersecurity enthusiasts, and anyone building a career in technology.

**Course** – Introduction to Networking Essentials
**Audience** – Beginners, home users, IT support staff, and anyone seeking a solid foundation in network design, configuration, and troubleshooting
**Duration** – 22 Hours
**Platform** – Cisco Networking Academy
**Lab Environment** – Cisco Packet Tracer

---

## Course Purpose

The Networking Basics course teaches the fundamentals of networking by covering the basic concepts and skills needed to set up and manage your small office or home office (SOHO) network. The learner is presented with an engaging and exploratory view of networks, the devices that comprise them, how they work, and basic troubleshooting tools and techniques.

Upon completion of the Networking Basics course, students will be able to:

- Explain important concepts in network communication
- Explain network types, components, and connections
- Configure mobile devices for wireless access
- Configure an integrated wireless router and wireless client to connect securely to the internet
- Explain the importance of standards and protocols in network communications
- Describe common network media
- Explain how communication occurs on Ethernet networks
- Explain the features of an IP address
- Explain how IPv4 addresses are used in network communication and segmentation
- Explain features of IPv6 addressing
- Configure a DHCP server
- Explain how routers connect networks together
- Explain how ARP enables communication on a network
- Create a fully connected LAN
- Explain how clients access internet services
- Explain the function of common application layer services
- Use various tools to test and troubleshoot network connectivity

---

## Repository Structure

This repository is organized as an Obsidian vault with the following structure:

```
Networking-Basics-By-Cisco/
├── Networking Basics/          # Core course modules (Modules 01-17)
│   ├── Module 01/             # Communication in a Connected World
│   ├── Module 02/             # Network Components & Connectivity
│   ├── Module 03/             # Wireless Networks & Mobile Connectivity
│   ├── Module 04/             # Home Network & Wireless Setup
│   ├── Module 05/             # Communication Protocols & Standards
│   ├── Module 06/             # Network Media Types
│   ├── Module 07/             # Encapsulation & Ethernet
│   ├── Module 08/             # IPv4 Addressing Fundamentals
│   ├── Module 09/             # IPv4 Types & Network Segmentation
│   ├── Module 10/             # IPv4 Issues & IPv6 Addressing
│   ├── Module 11/             # DHCP Configuration
│   ├── Module 12/             # Network Boundaries & NAT
│   ├── Module 13/             # MAC & ARP Protocol
│   ├── Module 14/             # Routing Fundamentals & LAN Design
│   ├── Module 15/             # Application Services & Internet Access
│   ├── Module 16/             # Transport Layer Protocols
│   └── Module 17/             # Troubleshooting Commands & Tools
├── Cisco Packet Tracer/       # CPT tutorials and guides
│   ├── Section 1/             # CPT Fundamentals (1.1-1.6)
│   └── Section 2/             # Basic Network Construction (2.1-2.3)
├── Cheatsheets/               # Quick reference materials
│   └── Cheatsheet-Networking.md  # Dynamic command reference with DataviewJS
├── RoadMap/                   # Course overview and learning path
├── Images/                    # Supporting images and diagrams
└── Imagesn/                   # Additional screenshots and visuals
```

### What's Included

- **76 Markdown files** with detailed notes and explanations
- **17 Anki flashcard decks** (.apkg files) with 500+ spaced repetition cards
- **15 Cisco Packet Tracer labs** (.pka files) with hands-on exercises
- **100+ images** and network diagrams for visual learning
- **Dynamic cheatsheet** that aggregates commands from all modules
- **Automated TOC generation** for easy navigation
- **Complete Obsidian vault configuration** for optimal note-taking

---

## Learning Outcomes

After completing this course you will be able to:

1. Explain how data moves through a network
2. Identify and differentiate between network devices and media
3. Securely configure mobile devices for Wi-Fi
4. Set up an integrated wireless router for safe Internet access
5. Apply IPv4/IPv6 addressing and subnetting
6. Deploy and manage a DHCP server
7. Configure basic static routes and understand router function
8. Use ARP to troubleshoot local network communication
9. Build a fully connected LAN that meets user requirements
10. Resolve connectivity issues with ping, traceroute, and packet captures

---

## Prerequisites

- Basic computer literacy (file navigation, command prompt/terminal usage)
- **Cisco Packet Tracer** – If you haven't used it before, [take this short course](https://www.netacad.com/courses/getting-started-cisco-packet-tracer?courseLang=en-US)
  - You can also check out the [Cisco Packet Tracer notes](Cisco%20Packet%20Tracer/) included in this repository
- **Anki** (recommended for flashcard study) – [Download here](https://apps.ankiweb.net/)
- Internet connection for downloading labs and resources
- **Obsidian** (optional but recommended) – [Download here](https://obsidian.md/download)

---

## Getting Started

### Option 1: Use with Obsidian (Recommended)

Follow these steps to open the **Networking Basics** course as an Obsidian vault:

1. **Download Obsidian**
   Get Obsidian for your platform: [https://obsidian.md/download](https://obsidian.md/download)

2. **Clone or Download the Repository**

   **Option A – Clone using Git** (recommended):
   ```bash
   git clone https://github.com/mohsinkhadim59/Networking-Basics-By-Cisco.git
   ```

   **Option B – Download ZIP**:
   - Visit the [repository](https://github.com/mohsinkhadim59/Networking-Basics-By-Cisco)
   - Click **Code → Download ZIP**
   - Unzip the downloaded file

3. **Open the Course in Obsidian**
   - Launch **Obsidian**
   - Click **Open folder as vault**
   - Select the folder: **Networking-Basics-By-Cisco**
   - Obsidian will load all course notes, labs, and resources

### Option 2: Browse on GitHub

You can browse the notes directly on GitHub, though you'll miss out on Obsidian's linking and navigation features:

- Navigate to [Networking Basics](Networking%20Basics/) for course modules
- Check out [Cisco Packet Tracer](Cisco%20Packet%20Tracer/) for CPT tutorials
- View the [Networking Cheatsheet](Cheatsheets/Cheatsheet-Networking.md) for quick command reference

---

## Course Modules

The course is divided into 17 comprehensive modules:

| Module | Topic | Key Concepts |
|--------|-------|--------------|
| **01** | Communication in a Connected World | Network types, data transmission, bandwidth/throughput |
| **02** | Network Components & Connectivity | Clients/servers, network components, ISP connectivity |
| **03** | Wireless Networks & Mobile Connectivity | Wireless networks, mobile device connectivity |
| **04** | Home Network & Wireless Setup | Home router setup, wireless standards |
| **05** | Communication Protocols & Standards | Protocols, standards, OSI/TCP-IP models |
| **06** | Network Media Types | Copper, fiber, wireless media |
| **07** | Encapsulation & Ethernet | Ethernet frames, access layer |
| **08** | IPv4 Addressing Fundamentals | IPv4 purpose and structure |
| **09** | IPv4 Types & Network Segmentation | Unicast/broadcast/multicast, network segmentation |
| **10** | IPv4 Issues & IPv6 Addressing | IPv4 limitations, IPv6 introduction |
| **11** | DHCP Configuration | Static/dynamic addressing, DHCP setup |
| **12** | Network Boundaries & NAT | Network boundaries, NAT configuration |
| **13** | MAC & ARP Protocol | MAC addresses, ARP protocol |
| **14** | Routing Fundamentals & LAN Design | Routing tables, LAN creation |
| **15** | Application Services & Internet Access | DNS, web servers, FTP, email, virtual terminals |
| **16** | Transport Layer Protocols | TCP, UDP, port numbers |
| **17** | Troubleshooting Commands & Tools | ipconfig, ping, traceroute |

---

## Hands-On Labs

This repository includes 15 Cisco Packet Tracer labs distributed across modules:

- Configure a Wireless Router and Client (Module 04)
- Connect to a Web Server (Module 08)
- Configure DHCP on a Wireless Router (Module 11)
- Examine NAT on a Wireless Router (Module 12)
- Identify MAC and IP Addresses (Module 13)
- Create a LAN (Module 14)
- Observe Traffic Flow in a Routed Network (Module 14)
- Observe Web Requests (Module 15)
- The Client Interaction (Module 15)
- Use the ipconfig Command (Module 17)
- Use the ping Command (Module 17)
- Create a Simple Network (Cisco Packet Tracer section)

---

## Anki Flashcards

This repository includes **17 Anki flashcard decks** (one for each module) with a total of **500+ flashcards** designed to help you retain networking concepts through spaced repetition learning.

### What's Included

Each module folder contains a `Module XX.apkg` file with:
- **Fill-in-the-blank questions** for active recall
- **Answer + Explanation format** for deeper understanding
- **20-38 flashcards per module** covering key concepts
- **Clean, readable design** with white text on dark background

### Getting Started with Anki

#### 1. Download Anki

Anki is a free, open-source flashcard application that uses spaced repetition to optimize learning.

- **Desktop (Windows/Mac/Linux)**: [https://apps.ankiweb.net/](https://apps.ankiweb.net/)
- **Android**: [AnkiDroid](https://play.google.com/store/apps/details?id=com.ichi2.anki) (Free)
- **iOS**: [AnkiMobile](https://apps.apple.com/us/app/ankimobile-flashcards/id373493387) (Paid, $24.99)

#### 2. Import Flashcard Decks

**Option A - Import Individual Modules:**
1. Open Anki on your device
2. Click **File → Import** (or press `Ctrl+Shift+I`)
3. Navigate to the module folder (e.g., `Networking Basics/Module 01/`)
4. Select the `.apkg` file (e.g., `Module 01.apkg`)
5. Click **Open** to import
6. Repeat for other modules you want to study

**Option B - Import All Modules at Once:**
1. Select all `.apkg` files from multiple module folders
2. Drag and drop them into the Anki window
3. Anki will import all decks automatically

#### 3. Start Studying

1. Click on a deck name (e.g., "Networking Basics - Module 01")
2. Click **Study Now**
3. Read each question and try to recall the answer
4. Click **Show Answer** to reveal the answer and explanation
5. Rate how well you knew the answer:
   - **Again** - You didn't know it (card will appear again soon)
   - **Hard** - You struggled to recall (shorter interval)
   - **Good** - You knew it (normal interval)
   - **Easy** - You knew it perfectly (longer interval)

#### 4. Sync Across Devices (Optional)

Keep your study progress synchronized across all your devices:

1. **Create a Free AnkiWeb Account**
   - Visit [https://ankiweb.net/account/register](https://ankiweb.net/account/register)
   - Sign up with your email

2. **Link Your Desktop Anki to AnkiWeb**
   - Open Anki on your computer
   - Click the **Sync** button (top right)
   - Enter your AnkiWeb credentials
   - Click **Upload** to send your decks to AnkiWeb

3. **Sync on Mobile Devices**
   - Open AnkiDroid (Android) or AnkiMobile (iOS)
   - Go to **Settings → AnkiWeb Account**
   - Enter your AnkiWeb credentials
   - Tap **Sync** to download your decks

4. **Keep Everything in Sync**
   - Always click **Sync** before and after studying
   - Your progress, new cards, and reviews will sync automatically
   - Works across unlimited devices with one free account

### Study Tips

- **Daily Reviews**: Study for 15-20 minutes each day for best retention
- **Complete Reviews**: Always finish your daily reviews before learning new cards
- **Module Progression**: Import new module decks as you complete the corresponding course material
- **Customize Settings**: Adjust daily new card limits in deck options (default: 20 cards/day)
- **Use Explanations**: Don't just memorize - read the explanations to understand the concepts

### Flashcard Coverage by Module

| Module | Deck Name | Cards | Key Topics |
|--------|-----------|-------|------------|
| 01 | Communication in a Connected World | 26 | Network types, data transmission, bandwidth |
| 02 | Network Components, Types and Connections | 25 | Clients/servers, P2P, ISP connectivity |
| 03 | Wireless Networks and Mobile Networks | 28 | Wi-Fi, wireless standards, security |
| 04 | Build a Home Network | 30 | Router setup, wireless configuration |
| 05 | Communications Principles | 38 | Protocols, standards, OSI/TCP-IP models |
| 06 | Network Media | 30 | Copper, fiber, wireless media |
| 07 | The Access Layer | 30 | Ethernet, encapsulation, MAC addresses |
| 08 | The Internet Protocol | 30 | IPv4 addressing, binary conversion |
| 09 | The IPv4 and Network Segmentation | 30 | Subnetting, broadcast domains |
| 10 | The IPv6 Addressing Formats and Rules | 31 | IPv6 structure, address types |
| 11 | Dynamic Addressing with DHCP | 30 | DHCP configuration, address assignment |
| 12 | Gateways to Other Networks | 30 | NAT, default gateway, routing |
| 13 | The ARP Process | 30 | ARP protocol, MAC-to-IP mapping |
| 14 | Routing Between Networks | 30 | Routing tables, LAN design |
| 15 | Application Layer Services | 30 | DNS, HTTP, FTP, email protocols |
| 16 | TCP and UDP | 30 | Transport protocols, port numbers |
| 17 | Network Testing Utilities | 30 | ipconfig, ping, traceroute |

---

## How to Use This Repository

1. **Start with the RoadMap** – Review [Phase-MAP.md](RoadMap/Cover/Phase-MAP.md) for course overview and learning outcomes
2. **Follow Module Sequence** – Work through modules 01-17 in order for a progressive learning experience
3. **Complete Labs** – Each module with a lab includes a `.pka` file; open it with Cisco Packet Tracer
4. **Study with Anki Flashcards** – Import the `.apkg` files into Anki for spaced repetition learning (see [Anki Flashcards](#anki-flashcards) section below)
5. **Use the Cheatsheet** – Reference [Cheatsheet-Networking.md](Cheatsheets/Cheatsheet-Networking.md) for quick command lookup
6. **Study with Obsidian** – Leverage bidirectional links, graph view, and search for optimal learning

---

## Features

- **Structured Learning Path** – 17 modules covering fundamentals to troubleshooting
- **Spaced Repetition Learning** – 500+ Anki flashcards for long-term retention
- **Hands-On Practice** – 15 Packet Tracer labs with real network scenarios
- **Visual Learning** – 100+ diagrams and screenshots
- **Dynamic Reference** – Auto-generated cheatsheet with commands from all modules
- **Obsidian Integration** – Wiki-style linking, graph view, and powerful search
- **GitHub Integration** – Version control, automated TOC generation
- **Multi-Device Sync** – Study flashcards anywhere with AnkiWeb synchronization
- **MIT Licensed** – Free to use, modify, and share

---

## Learning Resources

- **Cisco Networking Basics** – [NetAcad Curriculum](https://www.netacad.com/launch?id=f393c38f-b410-4d2b-8275-70e144273519&tab=curriculum&view=ae8638aa-428f-5d03-b275-742d5f1b805c)
- **Cisco Packet Tracer** – [Download & Get Started](https://www.netacad.com/courses/getting-started-cisco-packet-tracer?courseLang=en-US)
- **Anki** – [Download Anki](https://apps.ankiweb.net/) | [Anki Manual](https://docs.ankiweb.net/) | [AnkiWeb (Sync Service)](https://ankiweb.net/)
- **Obsidian Documentation** – [Help Vault](https://help.obsidian.md/)

---

## System Requirements

**For Obsidian:**
- Windows 10/11, macOS 12+, or Ubuntu 22.04/24.04 LTS
- amd64 (x86-64) CPU
- 4 GB RAM minimum
- 1.4 GB free disk space

**For Cisco Packet Tracer:**
- See [Cisco's official requirements](https://www.netacad.com/courses/packet-tracer)

---

## Contributing

Contributions are welcome! If you find errors, have suggestions, or want to add content:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -m 'Add improvement'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE.txt) file for details.

---

## Acknowledgments

- **Cisco Networking Academy** for the excellent course content
- **Obsidian** for the powerful note-taking platform
- The networking community for continued support and knowledge sharing

---

## Next Steps

After completing this course, consider:

- **Cisco CCNA** or **CompTIA Network+** certifications
- Practicing with real hardware (routers, switches, wireless access points)
- Advanced topics: VLANs, ACLs, NAT, VPNs, network security
- Building home lab environments for hands-on experimentation

---

Happy learning, and may your packets flow smoothly! 🚀

