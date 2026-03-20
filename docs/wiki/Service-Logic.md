# Service Logic

This page provides a technical deep-dive into how the six primary service offerings — **IT Management**, **Security Consulting**, **Energy Auditing**, **Office Tech Setup**, **UniFi Protect Setup**, and **Custom Project Requests** — are represented on the website and what they entail operationally.

---

## IT Management

### Overview

The IT Management service covers end-to-end network design, provisioning, and ongoing support with a focus on the **Ubiquiti UniFi ecosystem**.

### Workflow

```
1. Discovery Call      → Understand client's current infrastructure and goals
2. Site Survey         → Assess physical layout, existing hardware, ISP connection
3. Network Design      → Plan VLAN segmentation, AP placement, firewall rules
4. Hardware Procurement → Source UniFi switches, APs, UDM/USG, PoE injectors
5. Installation        → Rack/mount hardware, cable management, physical setup
6. Configuration       → UniFi Network controller setup, SSIDs, QoS, VPN (if needed)
7. UniFi Protect Setup → Camera/NVR configuration, recording schedules, zones
8. Handover & Training → Client walkthrough, documentation ("Dee-structions")
9. Ongoing Support     → Remote monitoring, firmware updates, troubleshooting
```

### Key Technologies

| Technology | Purpose |
|---|---|
| UniFi Network | Core LAN/WLAN management platform |
| UniFi Protect | IP camera and NVR management |
| UniFi Gateway (UDM/USG) | Routing, firewall, IDS/IPS |
| VLANs | Network segmentation (IoT, guest, corporate) |
| PoE Switches | Power delivery to APs and cameras |

### Website Representation

On the website, IT Management is displayed as one of six service cards in the `#services` section. The card uses the `fa-server` icon and lists skill bubbles (Consulting, Network Admin).

---

## Security Consulting

### Overview

Security Consulting focuses on **physical security audits** — assessing vulnerabilities that exist in the physical world rather than the digital realm.

### Workflow

```
1. Initial Assessment  → Identify scope (residential, commercial, multi-site)
2. Physical Walkthrough → Audit entry points, door hardware, locks, hinges
3. Access Control Review → Evaluate keypad/card/biometric systems
4. Circuit Security    → Inspect electrical panel access and breaker security
5. Reporting           → Deliver written findings with severity ratings
6. Remediation Guidance → Recommend hardware upgrades and procedural changes
```

### Key Areas Audited

- Door hardware (frame integrity, deadbolt quality, strike plates)
- Access control systems (keypads, smart locks, key fob systems)
- Perimeter security (lighting, camera blind spots, gate latches)
- Electrical panel and circuit access

---

## Energy Auditing

### Overview

Energy Auditing involves a technical assessment of a building's **envelope and electrical systems** to identify inefficiencies and recommend improvements.

### Workflow

```
1. Baseline Data Collection → Review utility bills, occupancy schedules
2. Building Envelope Audit  → Inspect insulation, windows, doors, HVAC air-locks
3. Lighting Audit           → Assess fixture types, wattage, occupancy logic
4. Curtain/Window Audit     → Evaluate thermal curtains and solar gain management
5. HVAC Systems Review      → Inspect ductwork sealing, thermostat programming
6. Report & ROI Analysis    → Prioritize recommendations by payback period
```

### Key Areas Assessed

| Area | What We Look For |
|---|---|
| HVAC Air-locks | Proper vestibule sealing to prevent conditioned air loss |
| Thermal Curtains | R-value, coverage, and automated scheduling |
| Lighting Logic | LED conversion opportunities, occupancy/daylight sensors |
| Building Envelope | Air infiltration, insulation gaps, thermal bridging |

### Website Representation

Energy Auditing is represented as a service card in the `#services` section using the `fa-bolt-lightning` icon, with skill bubbles for Efficiency and Infrastructure.

---

## Office Tech Setup

### Overview

Office Tech Setup covers the integration of workstations, printers, and peripherals for local business or home office environments. The focus is on professional hardware configuration, not physical installation or wiring.

### Workflow

```
1. Scope Assessment   → Identify devices, peripherals, and connectivity requirements
2. Hardware Setup     → Configure workstations, monitors, and printers
3. Network Join       → Connect devices to existing LAN/WLAN
4. Software Config    → Install and configure required software and drivers
5. Handover           → Client walkthrough and documentation
```

### Website Representation

Office Tech Setup is displayed as a service card using the `fa-laptop` icon, with skill bubbles for Workstations and Provisioning.

---

## UniFi Protect Setup

### Overview

UniFi Protect Setup covers the full configuration of Ubiquiti cameras and NVRs, including recording schedules, detection zones, and remote access setup on the client's existing hardware.

### Workflow

```
1. Hardware Audit     → Inventory existing cameras, NVR, and network topology
2. Protect OS Setup   → Configure UniFi Protect application on UDM/UNVR
3. Camera Adoption    → Add and name all cameras within the Protect UI
4. Recording Logic    → Set continuous vs motion-only schedules and retention
5. Detection Zones    → Define motion zones and activity detection regions
6. Remote Access      → Configure UniFi account access and mobile app connectivity
7. Handover           → Client walkthrough and access delegation
```

### Website Representation

UniFi Protect Setup is displayed as a service card using the `fa-video` icon, with skill bubbles for Surveillance and Protect OS.

---

## Custom Project Requests

### Overview

Custom Project Requests covers technical solutions that fall outside the standard service catalog. These are scoped individually based on the client's infrastructure and goals.

### Website Representation

Custom Project Requests is displayed as a service card using the `fa-screwdriver-wrench` icon. It links directly to the `#contact` section with a "Start a Custom Request" CTA rather than listing fixed skill bubbles.

---

## Service Cards — Implementation Notes

Each service is represented in `index.html` within the `#services` section as a grid card with:
- A `service-icon-box` container holding a Font Awesome icon
- An `<h3>` heading
- A `<p>` description paragraph
- A set of `skill-bubble` `<span>` tags for keyword tags (or a CTA link for Custom Project Requests)

To add a new service, duplicate an existing card block and update the icon class, heading, description, and skill bubbles accordingly.
