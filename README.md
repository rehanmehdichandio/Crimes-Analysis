# LAPD Crime Data Analysis

<image-card alt="Los Angeles Skyline" src="[https://github.com/rehanmehdichandio/Crimes-Analysis/blob/main/la_skyline.jpg]" ></image-card>

## Overview

This repository presents an exploratory data analysis (EDA) of crime patterns in Los Angeles, California, using data from the Los Angeles Police Department (LAPD). The analysis aims to identify key trends in crime timing, locations, and victim demographics to support better resource allocation for public safety.

The project is built around a Jupyter notebook (`notebook.ipynb`) that processes the dataset, generates visualizations, and extracts actionable insights. Data is sourced from the [LAPD Crime Data](https://github.com/rehanmehdichandio/Crimes-Analysis/blob/main/crimes.xlsx) portal, modified for this exercise.

**Note**: As of November 02, 2025, the analysis uses historical data up to 2023. For the latest statistics, refer to the [LAPD NIBRS Victims Dataset](https://github.com/rehanmehdichandio/Crimes-Analysis/blob/main/crimes.xlsx) (updated September 17, 2025) and [Crime Trends in California 2024](https://data-openjustice.doj.ca.gov/sites/default/files/2025-07/Crime%20In%20CA%202024%20final.pdf), which show a 1.7% increase in violent crime rates statewide from 2022 to 2023, with ongoing monitoring into 2025.

## Key Insights

Based on the dataset analysis:

- **Peak Crime Hour**: Crimes peak at **12:00 PM (noon)**, indicating midday as a high-risk period citywide. Recent 2025 reports confirm this pattern persists.

- **Night Crime Hotspot**: The **Central** area remains the primary hotspot for night crimes (10:00 PM–3:59 AM), with elevated rates in central neighborhoods compared to suburban areas. In 2025, Downtown LA reports a crime rate of ~25,580 per 100,000 residents—over seven times the city average.

- **Victim Age Demographics**: Working-age adults are disproportionately affected. Breakdown by age group (based on 2020–2023 data; 2025 trends suggest similar distributions with a noted increase in theft odds per decade of age):

  | Age Group | Number of Victims |
  |-----------|-------------------|
  | 26–34     | 47,470            |
  | 35–44     | 42,157            |
  | 45–54     | 28,353            |
  | 18–25     | 28,291            |
  | 55–64     | 20,169            |
  | 65+       | 14,747            |
  | 0–17      | 4,528             |

  Total analyzed incidents: ~165,715. For 2025 updates, gun violence victims decreased by 19% in 2024, but demographics remain skewed toward adults.

---

## Visualizations include:
- Countplot of crimes by hour.
- Value counts for victim age brackets.

---

## Dataset

- **Source**: [LAPD Open Data](https://data.lacity.org/) – Crime Data from 2020 to Present (modified subset).
- **File**: `crimes.csv` (~165k rows).
- **Key Columns**:

  | Column        | Description |
  |---------------|-------------|
  | `DR_NO`      | Unique record number (year + area ID + sequence). |
  | `Date Rptd`  | Report date (MM/DD/YYYY). |
  | `DATE OCC`   | Occurrence date (MM/DD/YYYY). |
  | `TIME OCC`   | Occurrence time (HHMM, 24-hour). |
  | `AREA NAME`  | Patrol area (e.g., Central, Hollywood). |
  | `Crm Cd Desc`| Crime type (e.g., THEFT OF IDENTITY). |
  | `Vict Age`   | Victim age (years). |
  | `Vict Sex`   | Victim sex (F/M/X). |
  | `Vict Descent`| Victim descent (e.g., B=Black, H=Hispanic). |
  | `Weapon Desc`| Weapon used (if any). |
  | `Status Desc`| Status (e.g., Investigation Continued). |
  | `LOCATION`   | Address. |

---

## Requirements

- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `jupyter`

