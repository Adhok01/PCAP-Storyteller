<h1 align="center">🛡️ PCAP Storyteller</h1>

<p align="center">
  <strong>The Forensic Detective for Students & Educators</strong>
</p>

<p align="center">
  Transform messy PCAP network traffic into an interactive, visual storyboard.<br/>
  Built from the ground up to make network forensics easy to teach, learn, and understand.
</p>

<p align="center">
  <img alt="status" src="https://img.shields.io/badge/status-active-brightgreen">
  <img alt="python" src="https://img.shields.io/badge/python-3.9%2B-blue">
  <img alt="flask" src="https://img.shields.io/badge/framework-Flask-black">
  <img alt="license" src="https://img.shields.io/badge/license-MIT-lightgrey">
</p>

---

## 🌟 Why PCAP Storyteller? (The Problem)

Traditional tools like **Wireshark** are built for experts but often overwhelm students with "data overload."

- **The Wireshark Problem** — 50,000 packets look like a confusing spreadsheet. It's hard to see the "story."
- **Our Solution** — We automatically **link** related events (DNS ➔ HTTP ➔ TLS) and use **heuristic intelligence** to flag hacker behavior, so you can focus on the investigation, not the noise.

---

## 🖥️ Application in Action

A tour through the live dashboard — from the raw attack graph to the exported forensics report.

### 🕸️ Interactive Attack Graph
Automatically links DNS queries, TCP connections, and HTTP requests into a single explorable node graph, so relationships between events are visible at a glance instead of buried in a packet list.

![Attack Graph](screenshots/01_attack_graph.png)

### 📊 Network Intelligence Dashboard
A real-time statistical breakdown of the capture — total events, unique sources, traffic-type distribution, and top talkers — giving investigators an immediate sense of scale and shape.

![Analytics Dashboard](screenshots/02_analytics_dashboard.png)

### 🔍 Deep-Dive Analytics
Drill further into top destinations and the most frequently used ports to spot anomalies such as unusual concentration of traffic on a single port.

![Analytics Details](screenshots/03_analytics_details.png)

### ☣️ Threat Intelligence Engine
Behavioral heuristics — not just signature matching — surface attack patterns like port scanning and DNS tunneling, each scored and labeled by severity (HIGH / MEDIUM / LOW).

![Threat Intelligence](screenshots/04_threat_intelligence.png)

### 🌍 Global Incident Map
Every IP address involved in the capture is geolocated and pinned on an interactive map, making it easy to see whether traffic is domestic or originating from unexpected regions.

![Global Incident Map](screenshots/05_global_map.png)

### ⏱️ Forensic Timeline
A high-resolution, chronological reconstruction of every network event, letting investigators replay the exact sequence of a session second by second.

![Forensic Timeline](screenshots/06_forensic_timeline.png)

### 📄 Export Forensics Report
Generate a polished executive summary — as a PDF or Word document — complete with event counts, detected patterns, and full transaction logs, ready to hand off or archive.

![Export Report](screenshots/07_export_report.png)

---

## 🎓 Educational Curriculum

A complete 9-module learning path lives in the `documentation/` folder:

| # | Module | Description |
|---|--------|--------------|
| 00 | [Intro & Problem Statement](documentation/00_Introduction_and_Problem_Statement.md) | Why forensics is hard and how we fix it |
| 01 | [Definitions & Terminology](documentation/01_Definitions_and_Terminology.md) | DNS as a phonebook, packets as envelopes |
| 02 | [Tech Stack & Libraries](documentation/02_Tech_Stack_and_Flask_Libraries.md) | Why we use Flask, Scapy, and Folium |
| 03 | [Parsing Pipeline Deep-Dive](documentation/03_Parsing_Pipeline_Deep_Dive.md) | The 2-pass engine explained |
| 05 | [Threat Detection Heuristics](documentation/05_Threat_Detection_Heuristics.md) | Behavioral analysis vs. virus databases |
| 08 | [Teaching Flow](documentation/08_Teaching_Flow_Curriculum.md) | A guide for classroom instruction |

---

## 🚀 Key Features

### 🕵️ The Investigator (Parser)
- **2-Pass Pipeline** — identifies conversations first, then analyzes protocol details
- **Intelligent Linking** — automatically correlates DNS queries with their resulting TCP/HTTP connections
- **Unified Handlers** — specialized "experts" for DNS, HTTP, TLS, ICMP, and more

### 🧠 The Security Guard (Threats)
- **Heuristic Engine** — detects port scanning and DNS tunneling via behavior, not just signatures
- **Risk Scoring** — calculates a math-based severity score (0–100) for every IP address

### 🌍 The Global View (Geomap)
- **Dual-API Strategy** — uses `ipinfo.io` and `ip-api.com` to map attackers globally
- **Interactive Leaflet Maps** — real-world "pins" showing where traffic originates

### 📄 The Reporter (Export)
- **One-Click Exports** — generate professional PDF or Word forensics reports
- **Complete Records** — includes event counts, detected patterns, and full transaction logs

---

## ⚡ Quick Start

### 📦 Proper Installation (Package Mode)
```bash
# This uses our simplified setup.py to fetch everything automatically
pip install .
```

### 🏃 Run the Application
```bash
python run.py
```
The application will start on **http://localhost:5000**

---

## 📁 Project Architecture (The Engine Room)

The project follows a modular "services" architecture for clarity:

```
PCAP-StoryTeller/
├── run.py                 # The Ignition Switch (Entry Point)
├── setup.py                # The Assembly Line (Installation)
├── documentation/           # The Classroom (Curriculum)
├── frontend/                # The Dashboard (User Interface)
└── backend/                 # The Engine Room (Analysis)
    ├── app.py               # Application Factory
    ├── data/                 # The Brain (Persistence & DataManager)
    ├── parsers/              # The Investigator (Packet Deep-Dive)
    │   ├── pcap_parser.py
    │   └── protocol_handlers.py
    └── services/             # Specialized Experts
        ├── threat_service.py
        ├── map_service.py
        └── report_generator.py
```

---

## 🔧 Supported Protocols

| Protocol | Status | Analogy |
|----------|--------|---------|
| **DNS** | ✅ Full | The network phonebook |
| **HTTP** | ✅ Full | Unencrypted web postcards |
| **HTTPS/TLS** | ✅ Full | Locked safes (SNI detection) |
| **TCP** | ✅ Full | Registered letters (ordered) |
| **ICMP** | ✅ Full | Calling "hello?" (ping) |

---

## 🗺️ Navigating the App

| Tab | Purpose |
|-----|---------|
| 🏠 **Home** | Interactive attack graph linking DNS, TCP, and HTTP events |
| 📈 **Analytics** | Traffic distribution, top talkers, top destinations, common ports |
| ☣️ **Threats** | Heuristic-based attack pattern detection with severity scoring |
| 🔎 **Search** | Query specific events, IPs, or domains across the capture |
| 🌐 **Map** | Geolocated view of every packet's origin and destination |
| ☰ **Timeline** | High-resolution chronological reconstruction of network events |
| 📤 **Report** | Export a professional PDF/Word forensics report |

---

<p align="center">Adhokshaja ❤️</p>