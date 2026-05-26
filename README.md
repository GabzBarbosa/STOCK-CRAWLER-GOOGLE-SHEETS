# Marketplace Availability Monitor

Automated marketplace product availability monitoring integrated with Google Sheets.

---

# Overview

Marketplace Availability Monitor is an operational automation tool developed to monitor product availability at scale within marketplace environments such as Netshoes.

The solution automates the verification of product pages, identifying stock availability, unavailable products, HTTP errors and catalog issues, while updating operational results directly into Google Sheets.

This project was designed to reduce manual operational workload and improve catalog visibility for marketplace operations teams.

---

# Problem

Marketplace operation teams often need to manually monitor thousands of product URLs to identify:

- unavailable products
- stock rupture
- removed pages
- broken catalog listings
- inactive SKUs

Manual verification is slow, repetitive and operationally expensive.

---

# Solution

This tool automates the monitoring process using Playwright and asynchronous processing to access product pages, detect availability signals and classify the product status automatically.

Results are centralized into Google Sheets for operational tracking and analysis.

---

# Features

- Automated product URL monitoring
- Asynchronous browser processing
- Concurrent page execution
- Google Sheets integration
- HTTP status tracking
- Automatic stock status classification
- Detection of unavailable products
- Batch updates to avoid API rate limits
- Human-like navigation simulation
- Operational logging

---

# Tech Stack

- Python
- Playwright
- AsyncIO
- Google Sheets API
- GSpread
- Google Colab
- Pandas

---

# Operational Flow

```text
Google Sheets
      ↓
URL Reading
      ↓
Automated Navigation
      ↓
HTML Analysis
      ↓
Status Detection
      ↓
Classification
      ↓
Google Sheets Update
```

---

# Status Detection

The system automatically identifies scenarios such as:

| Status | Description |
|---|---|
| DISPONIVEL | Product available for purchase |
| SEM ESTOQUE | Product temporarily unavailable |
| INDISPONIVEL | Product removed or unavailable |
| 404 | Page not found |
| VERIFICAR | Undefined status requiring manual validation |

---

# Expected Impact

- Reduction of manual operational workload
- Faster identification of unavailable products
- Scalable catalog monitoring
- Increased operational visibility
- Improved marketplace monitoring efficiency

---

# Technical Highlights

- Real browser automation using Chromium
- Controlled concurrency with semaphores
- Async architecture for scalability
- Optimized batch update strategy
- Native Google authentication
- Browser fingerprint simulation

---

# Project Structure

```bash
project/
│
├── crawler/
├── detectors/
├── sheets/
├── config/
├── logs/
├── main.py
├── requirements.txt
└── README.md
```

---

# Spreadsheet Structure

| Column | Description |
|---|---|
| A | Product URL |
| B | Product Status |
| C | HTTP Status |
| D | Page Title |
| E | Last Verification |
| F | Observation |

---

# Installation

## Install dependencies

```bash
pip install playwright gspread pandas
playwright install chromium
```

---

# Configuration

Update the following variables:

```python
GOOGLE_SHEET_NAME = "Crawler Netshoes"
MAX_URLS = 2000
CONCURRENT_PAGES = 3
HEADLESS = True
```

---

# Running the Project

```python
await main()
```

---

# Example Use Cases

- Marketplace catalog monitoring
- Seller operational tracking
- Stock rupture monitoring
- Product availability intelligence
- Operational automation workflows

---

# Roadmap

## Planned Improvements

- Real-time dashboard
- Slack notifications
- Discord alerts
- Historical tracking
- Price monitoring
- Criticality scoring
- API integration
- Monitoring dashboard
- Multi-marketplace support

---

# Product Vision

This project was designed as an operational intelligence tool focused on reducing repetitive manual processes and improving visibility within marketplace catalog operations.

The goal is to evolve the solution into a scalable marketplace monitoring platform capable of supporting operational and product decision-making.

---

# Future Improvements

- Modular architecture
- Database integration
- Containerization with Docker
- Cloud execution
- Monitoring metrics
- Error retry system
- Queue management
- Multi-thread orchestration

---

# Author

Gabriella Barbosa

Focused on Product Operations, Automation, AI and Marketplace Intelligence.

GitHub:
https://github.com/GabzBarbosa
