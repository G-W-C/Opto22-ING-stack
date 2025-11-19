# Opto22-ING-stack

##### This tutorial explains how to build an open-source historian using Opto22 Hardware, Node-RED, InfluxDB v2, and Grafana.

<img width="745" height="638" alt="image" src="https://github.com/user-attachments/assets/a0dae69b-d5ad-4278-a145-baa6aab12d40" />

## Overview
This architecture collects data from Opto22 controllers (groov EPIC or SNAP-PAC) using Node-RED running on the groov EPIC with ```node-red-contrib-pac``` nodes. Node-RED handles data ingestion and transformation, then sends the data to **InfluxDB** using the ```node-red-contrib-influxdb``` node for simplified transport to InfluxDB, where it is stored for historical logging. Grafana provides visualization and dashboards for analysis.
**EPIC → Node-RED → InfluxDB → Grafana**

The Docker stack for **InfluxDB** and **Grafana** must run on a separate **IPC**, **server**, or even a **Raspberry Pi 5 with NVMe storage**.

This stack is inspired by the MING stack (MQTT → Node-RED → InfluxDB → Grafana) but simplifies it by removing MQTT and other intermediate layers. It’s ideal for small to medium sites that need quick deployment, minimal configuration, and reliable historical logging with Grafana dashboards.

###### For SNAP-PAC users without a groov EPIC, Node-RED can be installed on the backend host by adding it to the ```docker-compose.yml```.
🚧 Todo: Add a SNAP-PAC folder containing a docker-compose.yml for non-EPIC architectures.

## Getting Started

### Prerequisites
- **Docker** and **Docker Compose** must be installed on the backend host.  
  For installation instructions, see the official Docker documentation: https://www.docker.com/get-started/

### Steps

1. **Download required files**  
   Place the following files on the backend host (IPC, server, or RPi5):
   - `docker-compose.yml` (for InfluxDB + Grafana)
   - `nginx.conf`

2. **Launch Docker services on the backend host**  
   Open a terminal in the project directory and run:

  ```
  docker compose up -d
  ```
* Navigate to:
  * Grafana: http://localhost
  * InfluxDB: http://localhost:8086


🚧 Todo:
### Setup Node-RED

### Setup InfluxDB

### Setup Grafana
