# 🧰 Zabbix Template for HPE Nimble / Alletra Storage Systems

This Zabbix template is designed to monitor multiple HP HPE Storage Systems, with a strong focus on **HPE Nimble Storage** — a system for which working templates are hard to find.

It leverages the **Nimble API** and only requires a **read-only API user** to operate. Simply configure the required **template macros**, and you're ready to go!

---

## 🔍 Discovery Rules

The template includes three primary discovery rules:

- **Controller Discovery**
- **Volumes Discovery**
- **Network Interfaces Discovery**


---

## 📊 Monitored Items

Once applied, the template will create and monitor the following items:

### 🗃️ Array Metrics
- Array Available Bytes (TiB)
- Array Usable Capacity (TiB)
- Array Used Storage

### 📈 Volume Performance (per volume)
- Read IOPS
- Write IOPS
- Combined IOPS
- Read Latency
- Write Latency
- Combined Latency
- Read Throughput
- Write Throughput
- Combined Throughput
- Volume Size (GiB)
- Volume Mapped Usage (GiB)
- Volume Used (%)
- Volume Pool Latency

### 🧠 Controllers
- Controller A State
- Controller B State

### 🌐 Network
- Network Interface Status (per interface)

### 🔔 General Metrics
- Service Ping
- Get Alarms
- Get Arrays
- Get Controllers
- Get Data
- Get Network Interfaces
- Get Replication Partners
- Get Volumes

---

## ⚠️ Triggers

The template includes built-in triggers for:

- **Network link status** (per interface)
- **Volume usage** reaching near full capacity


---

## ✅ Requirements

- **Zabbix Version**: 6.x or higher recommended
- **HPE Nimble API Access**: A read-only API user
- **Template Macros**: Required for connecting to the Nimble API (e.g., host, username, password/token)
