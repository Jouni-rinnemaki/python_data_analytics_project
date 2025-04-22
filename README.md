# **Cyber Czech 2019 Exercise Analysis**

This repository contains a Jupyter Notebook that walks through the analysis of network traffic and log data captured during the March 2019 Cyber Czech red‑team/blue‑team exercise.
Repository Structure
```
.
├── cz.muni.csirt.IPFlowEntry/
│   └── data.json.gz
├── cz.muni.csirt.SyslogEntry/
│   └── data.json.gz
├── cz.muni.csirt.WinlogEntry/
│   └── data.json.gz
├── auxiliary-material/
│   ├── redteam-reserved-ip-ranges.csv
│   └── redteam-attack-schedule.csv
├── mini_project_rinnemaki.ipynb
└── README.md
```
## Data Sources

**IPFIX flows:** enriched NetFlow records in data.json.gz

**Syslog:** Linux log messages in data.json.gz

**Winlog:** Windows Event XML in data.json.gz

**Auxiliary:** Red‑Team IP ranges and attack schedule CSVs

## Summary of Analysis

- Loading & Cleaning Chunk‑streamed JSON‑gz files, normalized timestamps to Europe/Prague.

- Tagging Red Team Flagged flows and log entries containing known Red‑Team IPs or hostnames.

- Descriptive Statistics Counted ~140 k flows, ~6 M syslog entries; extracted Winlog severity from XML.

- Time‑Series Visualization Hourly plots show initial network spikes then service‑level log surges on both days.

- Severity Breakdown Syslog severity levels reveal many informational logs and a tail of warnings/errors.

- Unified Timeline Combined all Red‑Team events into one chronological view for end‑to‑end reconstruction.

## Future Work

**Protocol Analysis** – drill into IPFIX application protocols.

**Anomaly Detection** – build baselines and detect deviations.

**Cross‑Dataset Correlation** – link flows, syslog, and winlog by session or time.

**Machine Learning** – classify malicious vs. benign events.

**Interactive Dashboard** – real‑time filtering and drill‑down (Streamlit, Dash).

## **Mini‑Project for Python for Data Analytics & Statistics, Metropolia UAS (Spring 2025).**
