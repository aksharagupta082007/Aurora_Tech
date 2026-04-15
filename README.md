
````md
# Aurora_Tech

Aurora_Tech is an AI-powered disaster management platform built to support **hyperlocal disaster detection, analysis, and response**. The system is designed to improve emergency coordination during disasters such as **earthquakes** and **floods** by combining official alerts, smartphone sensor signals, geospatial data, and real-time citizen reports.

The goal is to enable faster and smarter disaster response through impact estimation, survivor intelligence, rescue prioritization, and safe route planning.

---

## Problem Statement

Natural disasters often lead to large-scale damage, loss of life, and delayed emergency response. One of the biggest challenges in disaster management is the lack of **real-time, hyperlocal information**. Traditional systems are often centralized, slow, and reactive, making them less effective in rapidly evolving situations.

Aurora_Tech aims to address this gap by building a system that can:

- collect local disaster-related evidence,
- verify incidents using multiple data sources,
- estimate severity and affected regions,
- identify probable survivor zones,
- prioritize rescue efforts, and
- support authorities with safer routing and real-time monitoring.

---

## Proposed Solution

Aurora_Tech uses a multi-layered AI-assisted workflow for disaster response.

The platform combines:

- **official alerts or simulated triggers**
- **smartphone sensor data**
- **GPS and location signals**
- **citizen distress reports**
- **population and infrastructure data**
- **geospatial road and building layers**

Using this data, the system can verify incidents, assess local severity, generate impact zones, identify survivor clusters, and provide rescue support through prioritization and routing.

---

## Key Features

- Hyperlocal disaster evidence collection
- Disaster verification using multiple signals
- Local severity estimation
- Impact zone mapping
- Survivor heatmaps and clustering
- Rescue prioritization for critical locations
- Safe route optimization for responders
- Citizen disaster reporting mode
- Real-time responder dashboard
- Scalable and modular system design

---

## System Workflow

```text
Official Alert / Simulated Trigger
                ↓
Hyperlocal Data Collection
                ↓
Signal Processing & Feature Extraction
                ↓
Multi-Factor Verification
                ↓
Impact Zone Estimation
                ↓
Survivor Intelligence
                ↓
Rescue Priority Scoring
                ↓
Dispatch & Route Optimization
                ↓
Citizen + Responder Dashboard
````

---

## Architecture Overview

The project is structured around the following major layers:

### 1. Hyperlocal Data Collection Layer

Collects information from:

* smartphone sensors
* GPS/location data
* distress reports
* population density data
* roads and building maps
* known risk zones

### 2. Data Ingestion Layer

Handles:

* API-based ingestion
* event parsing
* storage in PostgreSQL/PostGIS
* structured preprocessing

### 3. Incident Detection Layer

Performs:

* signal processing
* feature extraction
* anomaly analysis
* multi-factor verification

### 4. Impact & Survivor Intelligence Layer

Generates:

* affected area estimation
* geospatial overlays
* survivor heatmaps
* survivor clusters

### 5. Rescue Prioritization Layer

Ranks rescue zones based on:

* severity
* population
* vulnerability
* accessibility
* urgency

### 6. Routing & Allocation Layer

Supports:

* road-network-based route planning
* rescue allocation
* safer response navigation

### 7. Dashboard Layer

Provides:

* live incident visualization
* rescue priorities
* survivor hotspots
* operational insights for responders

---

## Tech Stack

### Backend

* FastAPI
* Python

### Data Processing

* Pandas
* NumPy
* SciPy

### Geospatial Tools

* GeoPandas
* Shapely
* PostGIS
* OpenStreetMap

### Routing and Network Analysis

* NetworkX
* pgRouting

### Database

* PostgreSQL
* PostGIS

### Frontend / Visualization

* React
* Mapbox
* Leaflet

### Data Sources

* Physics Toolbox CSV import
* Phyphox live polling
* smartphone sensor streams
* citizen reports
* official alerts / simulated alerts

---

## Implementation Pipeline

### Data Foundation

The system begins with geospatial and contextual datasets such as OpenStreetMap layers, population information, and disaster-related inputs.

### Data Ingestion

Incoming sensor streams, reports, and event data are parsed and stored through backend APIs.

### Incident Detection

Sensor features and contextual evidence are used to verify whether a disaster event has occurred.

### Impact Estimation

The platform estimates affected regions using geospatial operations and contextual overlays.

### Survivor Intelligence

AI and analytics are used to identify probable survivor-rich areas using heatmaps and clustering techniques.

### Rescue Prioritization

Affected areas are ranked based on risk, severity, population, and vulnerability.

### Routing & Allocation

The system computes safer rescue routes and supports response planning.

### Response Dashboard

A map-based interface provides responders with real-time situational awareness.

---

## Expected Impact

Aurora_Tech is designed to improve emergency management through:

* **faster response** with real-time analysis
* **better survivor identification** using heatmaps and clusters
* **smarter prioritization** of high-risk zones
* **safer rescue routes** for response teams
* **improved coordination** through a unified dashboard

---

## Scalability and Future Scope

The system is designed to be modular and extensible. In future versions, it can be expanded to support:

* additional disaster types such as landslides and fires
* stronger ML-based incident verification
* wider IoT sensor integration
* multilingual citizen reporting
* larger regional or national deployment
* predictive risk estimation for preparedness

---

## Repository Structure

```text
Aurora_Tech/
│── backend/
│   ├── api/
│   ├── services/
│   ├── models/
│   ├── utils/
│   └── main.py
│
│── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   └── public/
│
│── data/
│   ├── raw/
│   ├── processed/
│   └── sample_inputs/
│
│── geospatial/
│   ├── layers/
│   ├── zones/
│   └── routing/
│
│── docs/
│── tests/
│── requirements.txt
│── README.md
│── .gitignore
```

---

## Getting Started

### Clone the repository

```bash
git clone https://github.com/aksharagupta082007/Aurora_Tech.git
cd Aurora_Tech
```

### Backend setup

```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Database setup

Create a PostgreSQL database and enable PostGIS:

```sql
CREATE DATABASE aurora_tech;
\c aurora_tech
CREATE EXTENSION postgis;
```

### Run the backend

```bash
uvicorn main:app --reload
```

### Frontend setup

```bash
cd frontend
npm install
npm run dev
```

---

## Use Cases

### Earthquake Response

* official earthquake trigger
* nearby device corroboration
* hyperlocal severity estimation
* survivor cluster generation
* rescue prioritization

### Flood Response

* weather/flood trigger
* local reports and sensor support
* affected polygon estimation
* road and building risk analysis
* safe rescue route generation

---

## Contributors

* Akshara Gupta
* Riddhi Gopalani
* Tanvi Kadam
* Om Soparkar

**Team Name:** Aurora Tech

---

## License

This project is currently developed for academic, research, and prototype purposes.


---

## Repository Link

GitHub Repository:
[https://github.com/aksharagupta082007/Aurora_Tech](https://github.com/aksharagupta082007/Aurora_Tech)

```


