# <image src="assets/InAPickL_Logo.png" width=40></image> InAPickL

### An experimental cyberattack simulation and detection laboratory.

InAPickL is a cybersecurity project designed to simulate a small corporate network, execute controlled cyberattack scenarios, detect suspicious activity, and visualise security events through a centralised Security Operations Centre (SOC) dashboard.

The goal is to build a miniature digital twin of a corporate environment where attacks can be safely simulated, monitored, investigated, and responded to.

---

## Project Goals

- Build an isolated virtual corporate network.
- Simulate realistic cyberattack scenarios.
- Collect and analyse network and system events.
- Detect suspicious behaviour using custom detection rules.
- Visualise attacks and security alerts through a SOC dashboard.
- Investigate incidents and track their lifecycle.
- Implement automated defensive responses.
- Measure detection performance and false-positive rates.

## Architecture

InAPickL consists of five main components:

| Component | Responsibility |
|---|---|
| Attack Simulator | Executes controlled attack scenarios. |
| Monitoring System | Collects network and system events. |
| Detection Engine | Analyses events and identifies suspicious activity. |
| Incident Manager | Creates, tracks, and manages security incidents. |
| SOC Dashboard | Displays alerts, incidents, and network activity. |

### Technology Stack

**Backend**
- Python
- FastAPI
- SQLAlchemy
- Scapy
- NetworkX

**Frontend**
- React
- TypeScript
- Vite
- Tailwind CSS
- Recharts
- Cytoscape.js

**Infrastructure**
- Docker
- Docker Compose
- PostgreSQL
- Redis

**Testing**
- Pytest
- Vitest

## Planned Features

### 1. Network Simulation
A virtual corporate environment containing simulated workstations, servers, and databases.

### 2. Attack Simulation
Controlled scenarios including:

- Port scanning
- Brute-force login attempts
- Suspicious network traffic
- DDoS-like traffic patterns
- Suspicious file activity
- Privilege escalation indicators

### 3. Threat Detection
A custom detection engine that analyses incoming events and identifies potentially malicious behaviour.

### 4. SOC Dashboard
A central dashboard displaying:

- Live security alerts
- Active incidents
- Network topology
- Attack activity
- Event timelines
- Severity levels
- Detection statistics

### 5. Incident Response
Incident management functionality, including:

- Alert investigation
- Incident classification
- Severity assignment
- Incident status tracking
- Simulated defensive actions
- Audit logging

## Project Structure

```text
InAPickL/
│
├── backend/
│   └── app/
│       ├── api/
│       │   └── routes/
│       ├── core/
│       ├── database/
│       ├── detection/
│       ├── monitoring/
│       ├── services/
│       └── simulator/
│           └── scenarios/
│
├── frontend/
│   └── src/
│       ├── components/
│       ├── hooks/
│       ├── pages/
│       ├── services/
│       └── types/
│
├── simulation/
│
├── infrastructure/
│
├── docs/
│
├── docker-compose.yml
├── .env.example
└── README.md
```

## Getting Started

### Prerequisites

Install the following:

- Docker Desktop
- Python 3.12+
- Node.js 22+
- Git

### Clone the Repository

```bash
git clone https://github.com/28-aditya/InAPickL.git
cd InAPickL
```

### Configure Environment Variables

Create a `.env` file using the example:

```bash
cp .env.example .env
```

Configure the required environment variables before starting the services.

### Start the Environment

```bash
docker compose up --build
```

The frontend, backend, database, and supporting services will start through Docker Compose.

*Note: The isolated simulation network and its services will be configured separately as the project develops.*

## Development Roadmap

- [ ] **Phase 1:** Project setup and infrastructure
- [ ] **Phase 2:** Build the simulated corporate network
- [ ] **Phase 3:** Implement attack simulation scenarios
- [ ] **Phase 4:** Develop event collection and monitoring
- [ ] **Phase 5:** Build the detection engine
- [ ] **Phase 6:** Develop the SOC dashboard
- [ ] **Phase 7:** Implement incident management and response
- [ ] **Phase 8:** Testing, documentation, and performance evaluation

## Security & Ethical Considerations

InAPickL is intended strictly for educational purposes, cybersecurity research, and defensive security testing.

All attack simulations must take place within an isolated, controlled environment. The project must not be used to target systems, networks, or individuals without explicit authorisation.

## Future Improvements

Potential future additions include:

- MITRE ATT&CK framework mapping
- Machine-learning-assisted anomaly detection
- PCAP upload and analysis
- User authentication and role-based access control
- Advanced attack visualisation
- Threat intelligence integration
- Detection accuracy and performance metrics

---

## The Idea

**Simulate it. Detect it. Investigate it. Stop it.**

Welcome to InAPickL.
