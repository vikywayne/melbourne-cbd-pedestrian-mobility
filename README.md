# Melbourne CBD Pedestrian Activity and Free Public Transport Initiative (2025–2026)

## Project Overview

This project investigates pedestrian activity patterns within Melbourne CBD and explores whether Victoria's temporary free public transport initiative during April and May 2026 was associated with changes in pedestrian movement throughout the city.

Using pedestrian sensor data collected by the City of Melbourne, the analysis examines overall activity levels, location-specific changes, hourly movement patterns and weekday activity trends. The project demonstrates how publicly available urban sensor data can be used to evaluate city activity and support evidence-based policy discussions.

---

## Research Question

How were Melbourne CBD pedestrian activity patterns associated with Victoria's temporary free public transport initiative during April and May 2026?

### Supporting Questions

1. Did overall pedestrian activity change during the initiative period compared with February and March 2026?
2. Which sensor locations experienced the largest changes between April–May 2025 and April–May 2026?
3. Did activity patterns vary across different times of day?
4. Did pedestrian activity patterns vary by day of the week?

---

## Data Sources

### Dataset 1: Pedestrian Counting System – Monthly Counts Per Hour

This dataset contains hourly pedestrian counts collected from automated pedestrian sensors located throughout Melbourne CBD.

Files used:

* April 2025
* May 2025
* February 2026
* March 2026
* April 2026
* May 2026

### Dataset 2: Pedestrian Counting System – Sensor Locations

This supplementary dataset contains metadata describing pedestrian sensor locations, including:

* Sensor descriptions
* Geographic coordinates
* Operational status
* Installation and location information

The metadata was used to support data validation and provide contextual information about sensor locations.

---

## Project Files

| File                                            | Description                                                 |
| ----------------------------------------------- | ----------------------------------------------------------- |
| April_2025.csv                                  | Hourly pedestrian counts for April 2025                     |
| May_2025.csv                                    | Hourly pedestrian counts for May 2025                       |
| February_2026.csv                               | Hourly pedestrian counts for February 2026                  |
| March_2026.csv                                  | Hourly pedestrian counts for March 2026                     |
| April_2026.csv                                  | Hourly pedestrian counts for April 2026                     |
| May_2026.csv                                    | Hourly pedestrian counts for May 2026                       |
| pedestrian-counting-system-sensor-locations.csv | Sensor metadata dataset                                     |
| assignment.qmd                                  | Main Quarto document containing analysis and visualisations |
| README.md                                       | Project overview and supporting documentation               |

---

## Data Processing

The following processing steps were undertaken:

1. Imported monthly pedestrian count datasets and sensor metadata.
2. Audited dataset structure and data quality.
3. Converted non-standard missing values ("na" and "undefined") into standard missing values.
4. Combined monthly datasets into year-level datasets.
5. Identified sensors available in both 2025 and 2026.
6. Restricted year-to-year comparisons to common sensor locations.
7. Reshaped data from wide format into tidy long format.
8. Converted dates into a standard date format.
9. Created aggregated datasets for temporal and location-based analysis.

The final analysis dataset contains the following variables:

| Variable | Description                             |
| -------- | --------------------------------------- |
| Date     | Observation date                        |
| Hour     | Hour of day (0–23)                      |
| Sensor   | Pedestrian sensor location              |
| Count    | Number of pedestrian movements recorded |
| Year     | Observation year                        |

---

## Analysis Summary

The analysis focuses on four key areas:

### Overall Activity Trends

Examines daily pedestrian activity before and during the free public transport initiative to identify broad changes in city-wide movement patterns.

### Location-Level Changes

Identifies sensor locations that experienced the largest increases or decreases in pedestrian activity between April–May 2025 and April–May 2026.

### Hourly Activity Patterns

Compares average pedestrian activity throughout the day to determine whether movement patterns changed during the initiative period.

### Weekly Activity Patterns

Uses weekday-hour heatmaps to investigate whether pedestrian behaviour differed across weekdays and weekends.

---

## Limitations

Several limitations should be considered when interpreting the results:

* Sensor coverage changed between 2025 and 2026, requiring comparisons to be restricted to common locations.
* The analysis is observational and cannot establish causal effects of the transport initiative.
* Other factors such as weather conditions, tourism activity, special events and economic conditions may also influence pedestrian volumes.
* Some sensors contained missing observations that required cleaning prior to analysis.

---

## Software and Packages

The project was completed using:

* R
* Quarto
* tidyverse
* ggplot2
* janitor

---

## References

R Core Team. (2024). R: A language and environment for statistical computing. https://www.r-project.org/

Wickham, H., et al. (2019). Welcome to the tidyverse. Journal of Open Source Software, 4(43), 1686. https://doi.org/10.21105/joss.01686

City of Melbourne Open Data. (2026). Pedestrian Counting System – Monthly Counts Per Hour. City of Melbourne. Retrieved June 2026 from https://www.pedestrian.melbourne.vic.gov.au/

City of Melbourne Open Data. (2026). Pedestrian Counting System – Sensor Locations. City of Melbourne. Retrieved June 2026 from https://data.melbourne.vic.gov.au/explore/dataset/pedestrian-counting-system-sensor-locations/
