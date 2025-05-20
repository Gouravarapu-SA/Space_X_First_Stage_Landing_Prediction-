# 🚀 SpaceX Launch Data Analysis with Python

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![API](https://img.shields.io/badge/Data-REST_API-yellowgreen.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)

> A Python-powered data pipeline that fetches, processes, and analyzes historical launch data from SpaceX using its public REST API. This project focuses on extracting technical and operational launch parameters for further study and visualization.

---

## 📊 Overview

This notebook retrieves detailed SpaceX launch data and decodes key mission elements such as:

- 🚀 Rocket names and versions
- 📍 Launch site coordinates and names
- 🛰️ Payload mass and orbit type
- 🧱 Rocket core reuse metrics and outcomes
- 📈 Mission success and failure metadata

The project leverages SpaceX's v4 API to enrich datasets using HTTP requests and builds structured data tables for further use in machine learning, dashboards, or statistical analysis.

---

## 📁 Features

- 🔌 **Live API Integration** using `requests`
- 📦 **Data Enrichment**: joins launch data with rocket, payload, and core information
- 📍 **Geo-location**: extracts and maps launch site coordinates
- 🛰️ **Payload Details**: mass, orbit, and classification
- 🔁 **Reusability Metrics**: flight count, reuse status, landing success

---

## 🧪 Data Sources & Structure

- **API Endpoint**: `https://api.spacexdata.com/v4/launches/past`
- **Additional Endpoints Queried**:
  - `/rockets`
  - `/launchpads`
  - `/payloads`
  - `/cores`

### Example Structure:

```python
spacex_url = "https://api.spacexdata.com/v4/launches/past"
response = requests.get(spacex_url)
launch_data = response.json()
```

---

## 🧠 Data Enrichment Functions

The dataset is enriched using the following helper functions:

- `getBoosterVersion(data)`
- `getLaunchSite(data)`
- `getPayloadData(data)`
- `getCoreData(data)`

Each function performs an API lookup and appends new fields to the dataset, such as:

- 🚀 Booster name
- 📍 Launch site longitude and latitude
- 🛰️ Payload mass and orbit
- 🔁 Reuse count and landing success

---

## 🛠 Libraries Used

- `requests` – for HTTP API calls  
- `pandas` – for data manipulation  
- `numpy` – for numerical operations  
- `datetime` – to format launch dates  
- `json` – to handle API responses

---

## 🧠 Future Scope

- 🌐 Integrate visualization (e.g. launch maps with Folium or Plotly)  
- 📈 Create time series plots of mission frequency, reuse trends, or payload mass  
- 🧮 Feed data into ML models for mission success prediction  
- 🌍 Add a world map with launch sites and trajectories

---

## 📜 License

This project is licensed under the **MIT License**.  
Feel free to use, modify, and distribute it with proper attribution.

---

## 🙌 Acknowledgments

- [SpaceX API](https://github.com/r-spacex/SpaceX-API) – for access to public space launch data  
- Python open-source community – for the tools and libraries used

---

## 📫 Contact

For feedback, contributions, or questions:  
📧 **akhilsai96@gmail.com**
