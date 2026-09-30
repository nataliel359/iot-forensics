# IoT Forensics

A digital forensics research project investigating the **unique forensic characteristics, challenges, and investigation techniques associated with Internet of Things (IoT) devices**.

The project examines how traditional digital forensic principles apply to IoT environments, identifies challenges introduced by connected devices, and applies forensic investigation techniques to an IoT-focused scenario.

---

## Table of Contents

* [Overview](#overview)
* [Project Objectives](#project-objectives)
* [Why IoT Forensics?](#why-iot-forensics)
* [Investigation Approach](#investigation-approach)
* [Repository Structure](#repository-structure)
* [Key Concepts](#key-concepts)
* [IoT Forensic Challenges](#iot-forensic-challenges)
* [Hands-On Investigation](#hands-on-investigation)
* [Tools and Technologies](#tools-and-technologies)
* [Forensic Methodology](#forensic-methodology)
* [Evidence Considerations](#evidence-considerations)
* [Project Outcomes](#project-outcomes)
* [Skills Demonstrated](#skills-demonstrated)
* [Research Areas](#research-areas)
* [Future Improvements](#future-improvements)
* [Disclaimer](#disclaimer)
* [Author](#author)

---

## Overview

The **IoT Forensics** project explores the application of digital forensic principles to Internet of Things environments.

Unlike traditional computers and mobile devices, IoT devices can generate and transmit evidence across multiple locations and platforms. Relevant evidence may exist on the physical device, a companion smartphone, a local network, a cloud service, or within network communications.

This creates additional challenges for investigators attempting to:

* Identify potential sources of evidence
* Acquire data without unnecessarily altering it
* Preserve evidence integrity
* Analyze network and device activity
* Correlate evidence across multiple systems
* Determine where information is stored
* Understand proprietary IoT protocols and data formats
* Deal with encrypted communications
* Account for cloud-dependent services
* Maintain an appropriate forensic chain of custody

This project investigates these challenges and examines how forensic investigators can approach evidence collection and analysis in IoT environments.

---

## Project Objectives

The project is organized around three primary objectives.

### Objective 1 — Digital Forensics Fundamentals

Develop an in-depth understanding of traditional digital forensics, including:

* Digital evidence
* Evidence identification
* Evidence acquisition
* Evidence preservation
* Evidence analysis
* Evidence interpretation
* Reporting
* Chain of custody
* Forensic integrity
* Investigation methodologies

The purpose of this objective is to establish the traditional digital forensic foundation needed to evaluate how IoT investigations differ from conventional investigations.

### Objective 2 — IoT Forensic Characteristics and Challenges

Investigate the characteristics that make IoT forensics different from traditional digital forensics.

Areas of consideration include:

* Distributed evidence
* Heterogeneous hardware
* Embedded operating systems
* Limited local storage
* Proprietary technologies
* Cloud-based data
* Companion mobile applications
* Wireless communication
* Network traffic
* Encryption
* Volatile data
* Device accessibility
* Data ownership and privacy
* Evidence integrity
* Lack of standardized forensic procedures

### Objective 3 — Hands-On Forensic Investigation

Apply digital forensic concepts to an IoT investigation through practical evidence collection and analysis.

The hands-on portion focuses on identifying potential evidence sources, collecting available artifacts, analyzing data, and evaluating the effectiveness and limitations of traditional forensic tools and techniques when applied to IoT environments.

---

## Why IoT Forensics?

The growth of connected devices has created a rapidly expanding source of potential digital evidence.

IoT devices can include:

* Smart speakers
* Smart watches
* Fitness trackers
* Smart televisions
* Smart home appliances
* Security cameras
* Smart lighting
* Home automation systems
* Connected vehicles
* Medical devices
* Industrial control devices
* Wearable technology

An investigation involving one IoT device may therefore require examination of several interconnected components.

### Example Evidence Ecosystem

```text
                  ┌─────────────────┐
                  │    IoT Device   │
                  └────────┬────────┘
                           │
             ┌─────────────┼─────────────┐
             │             │             │
             ▼             ▼             ▼
       Local Storage   Network Traffic  Sensors
             │             │             │
             ▼             ▼             ▼
        Device Data    Router / PC    Generated Data
             │
             ▼
      Companion Mobile App
             │
             ▼
        Cloud Services
             │
             ▼
       Account / Logs
```

Evidence can therefore be distributed across the entire ecosystem rather than being contained within the IoT device itself.

---

## Investigation Approach

The project follows a research-to-practical-investigation approach.

```text
Research
   │
   ▼
Digital Forensics Fundamentals
   │
   ▼
IoT Forensic Characteristics
   │
   ▼
Identify IoT-Specific Challenges
   │
   ▼
Select Investigation Techniques
   │
   ▼
Collect Available Evidence
   │
   ▼
Analyze Artifacts
   │
   ▼
Evaluate Findings
   │
   ▼
Document Limitations & Recommendations
```

The investigation combines theoretical research with practical forensic analysis.

---

## Repository Structure

```text
iot-forensics/
│
├── Forensics Investigation.pptx
│
├── Objective 1 - In-Depth Understanding of Digital Forensics.docx
│
├── Objective 2 - In-Depth Understanding of the Characteristics
│   and Challenges of Digital Forensics in the Domain of IoTs.docx
│
├── Objective 3 - Hands-On Forensics Invstigation.docx
│
└── README.md
```

### `Objective 1`

Contains research into the foundations of digital forensics and the investigation process.

Topics include the principles and procedures used to identify, collect, preserve, analyze, and report digital evidence.

### `Objective 2`

Examines the characteristics and challenges associated specifically with digital forensics in IoT environments.

This section bridges traditional digital forensics and IoT-specific investigative requirements.

### `Objective 3`

Documents the practical component of the project, including the hands-on forensic investigation and analysis of available IoT evidence.

### `Forensics Investigation.pptx`

Presentation summarizing the project, investigation, and major findings.

---

# Key Concepts

## Digital Evidence

Digital evidence is information stored or transmitted in digital form that may be relevant to an investigation.

For IoT investigations, evidence may originate from multiple sources, including:

* IoT devices
* Smartphones
* Computers
* Routers
* Network infrastructure
* Cloud platforms
* Companion applications
* Application databases
* System logs
* Network captures

---

## Evidence Acquisition

Evidence acquisition involves collecting relevant data while minimizing alteration to the original evidence.

IoT acquisition can be particularly difficult because investigators may not have:

* Direct access to the device's storage
* Administrative privileges
* A supported forensic interface
* Documentation of the underlying hardware
* A standardized acquisition method

Investigators may therefore need to consider multiple acquisition sources rather than relying exclusively on the physical IoT device.

---

## Evidence Preservation

Evidence must be preserved in a manner that allows investigators to demonstrate that it has not been improperly altered.

Important considerations include:

* Maintaining original evidence
* Working from forensic copies when possible
* Recording acquisition procedures
* Documenting timestamps
* Recording device state
* Recording tool versions
* Maintaining hashes where applicable
* Maintaining chain-of-custody documentation

---

## Chain of Custody

A chain of custody records the handling of evidence throughout an investigation.

For IoT investigations, this can become more complicated because evidence may originate from multiple devices and services.

A documented evidence record should identify:

| Field              | Description                                    |
| ------------------ | ---------------------------------------------- |
| Evidence ID        | Unique identifier for the evidence             |
| Source             | Device, application, network, or cloud service |
| Acquisition Date   | Date and time evidence was acquired            |
| Acquisition Method | Method/tool used to obtain the evidence        |
| Investigator       | Person responsible for acquisition             |
| Hash               | Integrity verification value where applicable  |
| Storage Location   | Location of the preserved evidence             |
| Notes              | Relevant observations or limitations           |

---

# IoT Forensic Challenges

IoT investigations introduce several challenges that are less prominent in traditional computer forensics.

## 1. Heterogeneous Devices

IoT ecosystems contain devices with different:

* Hardware architectures
* Operating systems
* Firmware
* Storage technologies
* Communication protocols
* Authentication mechanisms
* Data formats

A forensic technique that works on one device may not work on another.

---

## 2. Distributed Evidence

Evidence may be distributed across:

```text
IoT Device
     │
     ├── Local Storage
     │
     ├── Companion Application
     │
     ├── Smartphone
     │
     ├── Router
     │
     ├── Network Traffic
     │
     └── Cloud Service
```

Investigators must determine which components may contain relevant artifacts.

---

## 3. Cloud Dependency

Many IoT devices rely heavily on cloud services.

Important information may therefore exist outside the physical device, including:

* Account information
* Device activity
* Event history
* Configuration information
* Logs
* Synchronization data
* User activity

This creates additional acquisition, authorization, privacy, and jurisdictional considerations.

---

## 4. Encryption

IoT communications may use encryption to protect information transmitted between:

* IoT devices
* Smartphones
* Routers
* Cloud services
* Other connected devices

Encrypted traffic can make network-level forensic analysis significantly more difficult.

---

## 5. Limited Local Storage

Some IoT devices have limited storage capacity and may not retain large amounts of historical information.

As a result, relevant evidence may need to be obtained from other sources within the ecosystem.

---

## 6. Proprietary Systems

Manufacturers may use proprietary:

* File systems
* Protocols
* APIs
* Data formats
* Authentication mechanisms
* Firmware
* Cloud architectures

Limited documentation can make forensic acquisition and interpretation difficult.

---

## 7. Volatile Evidence

Some IoT evidence may exist only temporarily.

Examples can include:

* Active network connections
* Memory contents
* Temporary logs
* Current device state
* Network sessions
* Dynamic IP information

Investigators must therefore consider the order and timing of evidence collection.

---

# Hands-On Investigation

The practical portion of the project applies forensic techniques to an IoT environment.

The investigation considers multiple potential evidence sources rather than treating the IoT device as an isolated system.

### Investigation Layers

```text
┌─────────────────────────────────────────┐
│              Cloud Evidence             │
├─────────────────────────────────────────┤
│           Application Evidence          │
├─────────────────────────────────────────┤
│             Network Evidence             │
├─────────────────────────────────────────┤
│              Device Evidence             │
├─────────────────────────────────────────┤
│          Companion Device Evidence       │
└─────────────────────────────────────────┘
```

Each layer can provide different pieces of information that may need to be correlated during an investigation.

---

## Evidence Collection

The investigation considers evidence that may be available from:

### Device-Level Evidence

Potential sources include:

* Device storage
* Firmware
* Configuration
* Device logs
* System artifacts
* User-generated data
* Device metadata

### Network-Level Evidence

Potential sources include:

* Packet captures
* IP addresses
* MAC addresses
* DNS requests
* Network protocols
* Connection endpoints
* Communication timing
* Application-layer traffic

### Mobile/Application Evidence

Companion applications may contain:

* Device identifiers
* Account information
* Configuration
* Cached information
* Application databases
* Activity history
* Authentication information

### Cloud Evidence

Potential sources include:

* Account activity
* Device logs
* Synchronization data
* Event history
* Cloud-stored configuration
* Service metadata

---

# Tools and Technologies

The project explores the use of digital forensic and network analysis techniques applicable to IoT environments.

Potential tools and technologies considered in the investigation include:

| Tool / Technology            | Purpose                                              |
| ---------------------------- | ---------------------------------------------------- |
| Wireshark                    | Network traffic capture and packet analysis          |
| Network analysis tools       | Identification and examination of IoT communications |
| Digital forensic suites      | Examination and analysis of acquired evidence        |
| Mobile forensic techniques   | Analysis of companion-device artifacts               |
| Firmware analysis techniques | Examination of embedded device data                  |
| Hashing                      | Evidence integrity verification                      |

> **Note:** The exact tools used for each investigation should be documented in the Objective 3 report, including versions, acquisition methods, and limitations.

---

# Forensic Methodology

A general IoT forensic workflow can be represented as:

```text
1. Preparation
      │
      ▼
2. Identification
      │
      ▼
3. Collection
      │
      ▼
4. Preservation
      │
      ▼
5. Examination
      │
      ▼
6. Analysis
      │
      ▼
7. Correlation
      │
      ▼
8. Documentation
      │
      ▼
9. Reporting
```

## 1. Preparation

Identify:

* Investigation scope
* Devices involved
* Potential evidence sources
* Available forensic tools
* Acquisition constraints

## 2. Identification

Determine:

* What devices are present
* How devices communicate
* Which applications are associated with them
* Which cloud services are involved
* Where evidence may exist

## 3. Collection

Acquire available evidence while minimizing unnecessary changes to the original data.

## 4. Preservation

Preserve collected evidence and document:

* Acquisition procedure
* Device state
* Timestamps
* Hash values
* Storage location
* Evidence handling

## 5. Examination

Process acquired evidence to identify relevant artifacts.

## 6. Analysis

Interpret artifacts and determine their significance to the investigation.

## 7. Correlation

Compare information from multiple sources.

For example:

```text
Device Event
     │
     ├── Timestamp
     │
     ▼
Network Connection
     │
     ├── IP / Domain
     │
     ▼
Mobile Application
     │
     ├── Recorded Activity
     │
     ▼
Cloud Service
     │
     └── Corresponding Event
```

Correlation can help establish relationships between seemingly independent artifacts.

## 8. Documentation

Record investigative procedures, observations, limitations, and findings.

## 9. Reporting

Present findings in a reproducible and understandable format.

---

# Evidence Considerations

IoT investigations should consider both **technical evidence** and **contextual evidence**.

### Technical Evidence

Examples include:

* Logs
* Packet captures
* Databases
* Metadata
* Firmware
* Device identifiers
* Network addresses
* Application artifacts
* Cloud records

### Contextual Evidence

Examples include:

* Device ownership
* Device configuration
* User accounts
* Device location
* Associated smartphones
* Network topology
* Time of activity
* Relationships between devices

The value of an artifact depends not only on what the artifact contains but also on how it relates to other evidence.

---

# Project Outcomes

This project demonstrates that IoT forensic investigations require investigators to look beyond the physical device.

Key areas explored include:

* Traditional digital forensic methodology
* IoT-specific forensic challenges
* Distributed evidence sources
* Network-based evidence
* Mobile companion applications
* Cloud-based evidence
* Data acquisition
* Evidence preservation
* Evidence integrity
* Artifact analysis
* Evidence correlation
* Forensic reporting

The project also highlights the limitations of applying traditional forensic approaches directly to heterogeneous IoT environments.

---

# Skills Demonstrated

This project demonstrates practical and research-oriented cybersecurity skills, including:

### Digital Forensics

* Digital evidence handling
* Evidence acquisition
* Evidence preservation
* Artifact analysis
* Chain of custody
* Forensic documentation
* Investigative methodology

### Network Forensics

* Network traffic analysis
* Packet inspection
* Network communication analysis
* Protocol identification
* Endpoint analysis

### IoT Security

* IoT architecture analysis
* Device ecosystem analysis
* IoT communication
* Cloud-connected devices
* Embedded systems
* IoT forensic challenges

### Security Research

* Literature review
* Technical research
* Comparative analysis
* Investigation methodology
* Documentation
* Technical reporting

### Analytical Skills

* Evidence correlation
* Problem solving
* Investigation planning
* Identifying investigative limitations
* Translating technical observations into findings

---

# Research Areas

The project intersects several cybersecurity disciplines:

```text
                 ┌───────────────────┐
                 │   IoT Forensics   │
                 └─────────┬─────────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
        ▼                  ▼                  ▼
 Digital Forensics   Network Forensics   IoT Security
        │                  │                  │
        └──────────────────┼──────────────────┘
                           │
                           ▼
                   Digital Evidence
                           │
                           ▼
                   Incident Investigation
```

Relevant research areas include:

* Digital forensics
* Network forensics
* Mobile forensics
* Cloud forensics
* IoT security
* Embedded systems security
* Digital evidence
* Incident response
* Cybercrime investigation
* Evidence preservation

---

# Future Improvements

Potential improvements to this project include:

* Expanding the number of IoT devices investigated
* Comparing multiple IoT manufacturers
* Developing a repeatable IoT forensic acquisition workflow
* Automating artifact extraction
* Performing deeper firmware analysis
* Investigating additional IoT communication protocols
* Expanding network traffic analysis
* Examining additional cloud-based artifacts
* Developing automated evidence correlation
* Creating standardized investigation checklists
* Testing forensic tools against additional IoT platforms
* Investigating anti-forensic considerations in IoT environments

A future implementation could also explore automation for identifying and correlating artifacts across multiple IoT evidence sources.

---

# Limitations

IoT forensic investigations can be constrained by:

* Limited access to device internals
* Proprietary hardware and software
* Encryption
* Limited documentation
* Cloud dependencies
* Device-specific storage mechanisms
* Limited forensic tool support
* Data volatility
* Privacy considerations
* Legal and authorization requirements

Therefore, the absence of an artifact should not necessarily be interpreted as proof that the corresponding activity did not occur.

---

# Responsible Use

This project is intended for **educational, research, and authorized forensic investigation purposes**.

Any forensic acquisition, network capture, device analysis, or examination of cloud accounts should be performed only on systems and data for which the investigator has appropriate authorization.

When conducting real-world investigations, investigators should follow applicable organizational policies, legal requirements, evidence-handling procedures, and professional forensic standards.

---

# Project Documentation

Detailed project materials are available in the repository:

* **[Objective 1 — In-Depth Understanding of Digital Forensics](./Objective%201%20-%20In-Depth%20Understanding%20of%20Digital%20Forensics.docx)**
* **[Objective 2 — Characteristics and Challenges of Digital Forensics in IoT](./Objective%202%20-%20In-Depth%20Understanding%20of%20the%20Characteristics%20and%20Challenges%20of%20Digital%20Forensics%20in%20the%20Domain%20of%20IoTs.docx)**
* **[Objective 3 — Hands-On Forensics Investigation](./Objective%203%20-%20Hands-On%20Forensics%20Invstigation.docx)**
* **[Forensics Investigation Presentation](./Forensics%20Investigation.pptx)**

---

# Author

**Natalie L.**

Computer Science graduate with an interest in:

* Cybersecurity
* Digital Forensics
* Red Teaming
* Network Security
* Incident Response
* Security Automation

---

## Project Focus

> **Investigating how digital forensic principles can be adapted to the unique and distributed evidence environment created by Internet of Things devices.**
