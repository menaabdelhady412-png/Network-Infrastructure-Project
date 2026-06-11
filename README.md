Network Topology & Infrastructure Design

🏢 **Project:** Campus Enterprise Network Architecture & Capacity Planning  

---

## 🌐 Overview
This repository contains the comprehensive enterprise-level network infrastructure design for Cairo University’s new 4-story (Ground + 3 Floors) Faculty of Computing & AI academic building. Adhering strictly to **TIA-568** and **TIA-569** standards, this project details a structured three-tier hierarchical architecture designed to ensure 100% wired connectivity, resilient high-availability wireless roaming, and multi-gigabit speeds.

The network layout delivers a minimum of 1 Gbps to individual desktops while utilizing a robust 10 Gbps vertical backbone structured to accommodate a 15–20 year building lifespan.

---

## ⚙️ Key Specifications & Requirements
* **Building Profile:** 3 floors + Ground floor server room, with roughly 1,500 m² of space per floor.
* **Physical Constraints:** Reinforced concrete construction with 3.5-meter ceiling heights.
* **Core Metrics:** Minimum of 2 outlets per work area or one outlet per 10 m² of usable space.
* **Scalability:** Mandatory 30% spare capacity factored into all endpoint allocations and switch port calculations.
* **Performance Targets:** Minimum 1 Gbps to desktop endpoints, 10 Gbps vertical backbone capacity, and redundant uplinks for critical zones.

---

## 🏗️ Network Topology & Architecture
The design implements a **Three-Tier Hierarchical Model** optimized for high availability, explicit traffic isolation, and fault tolerance:

* **Core & Distribution Layer:** Dual Layer 3 routing switches located within the Ground Floor server room, operating in an active/active state tied together by a high-speed **100 Gbps Stack Link**.
* **Access Layer:** Floor-level Telecommunications Rooms (TRs) housing stacks of 48-port Layer 2 Power over Ethernet (PoE+) switches.
* **Redundant Uplinks:** Each floor's switch stack links back to the Core Layer via **dual 10G LACP (Link Aggregation Control Protocol)** fiber connections to guarantee automated failover and aggregate bandwidth.

---

## 📊 Outlet & Port Calculations
To ensure hardware accuracy, 48-port switches are calculated at a usable capacity of 44 endpoint ports (reserving 4 ports per switch for uplink/redundancy configurations). A **1.30 multiplier** was applied across all baseline requirements for future expansion:

| Floor | Key Rooms & Facilities Covered | Base Ports | Required Ports (+30% Spare) | Hardware Required |
| :--- | :--- | :--- | :--- | :--- |
| **Ground Floor** | 2 Lecture Halls (100 seats each), Reception, Admin Offices | 20 ports | 26 ports | **1x** 48-Port Access Switch |
| **First Floor** | 1 Lecture Hall, 4 Tutorial Rooms, 2 Computer Labs, 10 Offices | 146 ports | 190 ports | **5x** 48-Port Access Switches |
| **Second Floor**| 1 Lecture Hall, 4 Tutorial Rooms, 2 Computer Labs, 15 Offices, Research Lab | 173 ports | 225 ports | **6x** 48-Port Access Switches |
| **Third Floor** | 6 Tutorial Rooms, 3 Computer Labs, 20 Offices, Library & Study Area | 216 ports | 281 ports | **7x** 48-Port Access Switches |
| **TOTAL** | **Entire Academic Infrastructure** | **555 ports** | **722 ports** | **19x 48-Port Access Switches** |

---

## 🛠️ Hardware & Media Specifications
* **Horizontal Cabling:** **Cat6a Unshielded Twisted Pair (U/UTP)**. Features internal plastic splines to isolate copper pairs, mitigate crosstalk, and support future 10 Gbps data delivery straight to desktops.
* **Backbone Cabling:** **OM4 Multimode Fiber Optic** paths utilizing Erika Violet outer jackets to distinguish the high-speed vertical framework from legacy systems visually.
* **Transceivers:** **10GBASE-SR SFP+ modules** connecting fiber backbone infrastructure directly into copper-based switch interfaces.
* **Patch Panels:** 48-port physical patch panels within TRs. All rigid, solid-core structural wall cables terminate here permanently, using flexible stranded patch cords to interface with active hardware—preventing structural strain on switch ports.
* **Pathway Routing:** Suspended cable trays running along the high ceilings, connecting to drops inside surface-mounted PVC conduits and wall ducts to preserve concrete structural integrity.

---

## 📶 Supplemental Wireless Layer
To supplement the 100% wired foundation, a mobile wireless infrastructure utilizes **Enterprise Wi-Fi 6E/7 Access Points (APs)**:

* **Seamless Roaming:** APs are structured with a **15% to 20% cell overlap**. The design initiates a sub-second roaming handoff as a device crosses the calculated -67 dBm signal threshold, preventing "sticky clients".
* **Co-Channel Interference (CCI) Mitigation:** Employs precise channel reuse configurations (Channels 1, 6, 11 on the 2.4 GHz band and staggered alternating bands on 5 GHz / 6 GHz).
* **Power Delivery:** APs are deployed via standard Cat6a runs utilizing **PoE+ (IEEE 802.3at)** directly out of floor-level access switches.

---

## 📌 Standards & Topologies Applied
* Hierarchical Three-Tier Campus Topology (Core, Distribution, Access Layers)
* TIA-568 (Commercial Building Telecommunications Cabling Standard)
* TIA-569 (Telecommunications Pathways and Spaces Standard)
* LACP (Link Aggregation Control Protocol) EtherChannel design
* High-density capacity planning and future-proofing scalability

---

## 👨‍💻 Team Members (Authors)
* **Mena Mohamed** (20245068)
* **Sophia Muhammad** (20247002)
* **Gehan Selim** (20245016)
* **Yara Altawashi** (20245098)
* **Sama Almasri** (20245110)
