# SIEM Dashboard

A full-stack Security Information and Event Management (SIEM) platform that provides real-time log ingestion, event correlation, alert management, and MITRE ATT&CK-based attack simulation.

The platform is designed to help users understand how modern Security Operations Centers (SOCs) monitor, detect, and investigate security events.

---

## Features

### Real-Time Log Monitoring

* Collect security events in real time
* Centralized event storage
* Searchable log viewer
* Live event updates

### Event Correlation Engine

Supports multiple detection rule types:

* Threshold Rules
* Sequence Rules
* Aggregation Rules

Automatically correlates events and generates alerts.

### Alert Management

* Alert generation
* Alert investigation workflow
* Alert acknowledgement
* Alert resolution
* False positive handling

### MITRE ATT&CK Simulation

Built-in attack simulation scenarios mapped to MITRE ATT&CK techniques:

* Brute Force Attack
* DNS Tunneling
* Phishing
* Privilege Escalation

### Dashboard Analytics

* Event Timeline
* Severity Breakdown
* Alert Statistics
* Top Event Sources
* Open Alert Tracking

---

## Architecture

```text
Browser (React)
        │
        ▼
      Nginx
        │
        ▼
   Flask Backend
        │
 ┌──────┴──────┐
 ▼             ▼
MongoDB      Redis
```

### Components

#### Frontend

* React 19
* TypeScript
* Vite
* TanStack Query
* Zustand

#### Backend

* Flask
* Gunicorn
* Pydantic

#### Data Layer

* MongoDB
* Redis Streams

#### Infrastructure

* Docker
* Docker Compose
* Nginx

---

## Project Structure

```text
siem-dashboard/
│
├── frontend/
├── backend/
├── conf/
├── assets/
├── learn/
├── compose.yml
└── README.md
```

---

## Quick Start

### Prerequisites

* Docker Desktop
* Docker Compose

Verify installation:

```bash
docker --version
docker compose version
```

---

### Clone Repository

```bash
git clone <repository-url>
cd siem-dashboard
```

---

### Create Environment File

```bash
cp .env.example .env
```

---

### Start the Platform

```bash
docker compose up -d
```

---

### Verify Containers

```bash
docker ps
```

Expected services:

```text
siem-nginx
siem-backend
siem-mongo
siem-redis
```

---

### Access Dashboard

Open:

```text
http://localhost:8431
```

---

## Available Pages

### Dashboard

Provides an overview of:

* Total Events
* Total Alerts
* Open Alerts
* Critical Alerts
* Event Timeline
* Severity Breakdown

### Log Viewer

Browse and investigate collected security events.

### Alerts

Manage and investigate generated alerts.

### Rules

View and manage event correlation rules.

### Scenarios

Launch attack simulations to generate security events and test detection logic.

---

## Technology Stack

| Layer            | Technology              |
| ---------------- | ----------------------- |
| Frontend         | React, TypeScript, Vite |
| Backend          | Flask, Gunicorn         |
| Database         | MongoDB                 |
| Cache/Streams    | Redis                   |
| Containerization | Docker                  |
| Reverse Proxy    | Nginx                   |

---

## Learning Objectives

This project demonstrates:

* SIEM Fundamentals
* Event Correlation
* Threat Detection
* Alert Management
* MITRE ATT&CK Mapping
* Dockerized Application Deployment
* Full-Stack Security Engineering

---

## Disclaimer

This project is intended for educational and research purposes. Attack simulations should only be executed in controlled environments and authorized systems.
