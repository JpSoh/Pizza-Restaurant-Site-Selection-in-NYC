# IBM Data Science Capstone Project: Optimal Pizza Restaurant Location in New York City

> **Coursera IBM Data Science Professional Certificate — Capstone Project**

A data-driven analysis that determines the best borough and neighbourhood in New York City to open a pizza restaurant, by combining crime statistics, population data, and venue information from the Foursquare API.

---

## 📋 Project Overview

### Purpose

This project tackles a hypothetical but practical business problem: a chef wants to open a pizza restaurant in New York City and needs to identify the borough and neighbourhood that will maximise return on investment. Rather than relying on intuition, the project uses a structured, data-driven approach — scoring boroughs on crime safety and population size, then narrowing down neighbourhoods based on venue density and competitive landscape.

### Key Features

- **Multi-factor Borough Selection** — Ranks all five NYC boroughs using a weighted scoring system based on crime rates (safety) and population counts (customer reach)
- **Neighbourhood-level Venue Analysis** — Uses the Foursquare API to measure the number of nearby venues as a proxy for foot traffic and spending power
- **Competitor Detection** — Identifies neighbourhoods where pizza restaurants are already among the top 10 most common venues, filtering them out to avoid saturated markets
- **Interactive Mapping** — Visualises borough and neighbourhood data on interactive Folium maps
- **K-Means Clustering (Bonus)** — Groups similar neighbourhoods using unsupervised machine learning, useful for planning future expansion with consistent marketing strategies

### Target Audience

- Entrepreneurs and restaurateurs evaluating where to open a food business in New York City
- Business analysts looking for a structured, data-driven site-selection framework
- Data science students and practitioners interested in applied geospatial analysis and clustering

---

## 📊 Methodology Summary

The analysis is structured into three stages:

1. **Data Pre-processing** — Collect, clean, and structure data from multiple sources (JSON, CSV, API) into analysis-ready formats
2. **Borough Selection** — Score each of the 5 NYC boroughs on crime safety and population size, then combine scores to pick the best borough
3. **Neighbourhood Selection** — Within the chosen borough, use Foursquare venue data to identify neighbourhoods with high commercial activity but low pizza restaurant competition

The result is a single recommended borough and neighbourhood: **Queens, Jackson Heights**.

---

## 📁 Project Files

| File / Folder | Description |
|---|---|
| `Documentations/Capstone Project Notebook.ipynb` | Main analysis notebook (NYC pizza restaurant location) |
| `Documentations/Capstone project presentation.pptx` | Presentation slides with flow charts and key findings |
| `Dataset/NYPD_Complaint_YTD_DataDictionary.xlsx` | Data dictionary for the NYPD crime complaint dataset |
| `Opening a restaurant in NYC.docx` | Written report with detailed methodology and discussion |
| `.env.example` | Template for Foursquare API credentials |
| `.gitignore` | Prevents `.env` and other sensitive files from being committed |
| `README.md` | This file |

---

## 📚 Technologies & Methods Used

- **Data Wrangling** — Cleaning, filtering, and merging datasets from JSON, CSV, and API sources
- **Exploratory Data Analysis** — Bar charts, pie charts, and summary statistics to understand distributions
- **API Integration** — Foursquare API for real-time neighbourhood venue data
- **Geospatial Visualisation** — Interactive Folium maps for spatial exploration
- **One-Hot Encoding** — Frequency analysis of venue categories per neighbourhood
- **Scoring Framework** — Custom ranking system to evaluate boroughs on multiple criteria
- **K-Means Clustering** — Unsupervised machine learning to group similar neighbourhoods

---

## ✅ Notes

- This notebook was built and executed inside **IBM Watson Studio** (now part of IBM watsonx.ai). It is not designed to be cloned and run locally — several cells rely on IBM Cloud Object Storage and Watson Studio-specific tooling that have been stripped out for sharing
- The notebook uses the **Foursquare API** (`CLIENT_ID`, `CLIENT_SECRET`, `VERSION`) for venue data — these credentials were removed by Watson Studio for sharing
- Results may vary if using a newer version of the crime dataset (the project uses the Feb 2020 snapshot)
- The K-Means clustering step is included as a bonus exploration and is not part of the main decision-making process
- This project was completed as part of the **IBM Data Science Professional Certificate** on Coursera
