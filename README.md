# Internet Shutdowns in India

**Data Pipeline and Dashboard on Recorded Internet Shutdowns, 2016–2025**

🔗 **[Explore the interactive dashboard](https://app.powerbi.com/links/m205wXRizt?ctid=4517da72-c8f7-4cec-b2fc-fda9fe4354f9&pbi_source=linkShare)**

`Python` `Pandas` `SQL` `Power BI`

---

## Problem Statement

The Indian government does not keep one central record of internet shutdown orders issued by states and Union Territories. Shutdown information is spread across different sources, which makes it hard to compare shutdowns by year, location, duration, reason, and network type.

## Project Objective

Turn public shutdown data into a clean, analysis-ready dataset and an interactive Power BI dashboard that shows how recorded shutdowns vary across time, place, duration, cause, and network.

**Research question:** What patterns can be observed in internet shutdowns in India in terms of frequency, duration, location, reported reason, and network type?

## Key Achievements

- Analyzed **920 recorded shutdown events** in India from 2016 to 2025.
- Built an end-to-end pipeline: Python cleaning → state extraction → date and duration processing → SQL analysis → Power BI.
- Automated data preparation so it can be repeated when a new version of the source data is released.
- Handled messy location data by keeping events that affect several states as **multi-state events** instead of forcing them into one state.
- Flagged invalid negative durations and excluded them from calculations instead of guessing values.
- Reported both **median and average duration**, because a few very long shutdowns distort the average.
- **Skills used:** Python (Pandas), SQL, Power BI, data cleaning, exploratory data analysis (EDA), and KPI design.

## Pipeline

```
Access Now Dataset → Python / Pandas → Data Cleaning → State Extraction
                   → Date and Duration Processing → EDA → SQL Analysis → Power BI Dashboard
```

## Dashboard Overview

The Power BI dashboard is a single-page decision-support view.

| Section | What it shows |
| --- | --- |
| 📊 **Key indicators** | Total recorded shutdowns, median duration, number of affected states and Union Territories, and longest recorded shutdown. |
| 📈 **Main visuals** | Shutdowns by year, shutdowns by state or Union Territory, duration distribution, reported causes, affected network, and restriction type. |
| 🎛️ **Filters** | Year, state or Union Territory, cause, network, and restriction type. |

## Data Preparation

1. **India filter:** Kept only records where `country = India`.
2. **Column selection:** Kept date, location, cause, duration, shutdown type, network affected, government justification, legal information, and event description.
3. **Dates:** Converted start and end dates to a standard format and created start year, start month, and month name columns.
4. **States:** Extracted state and Union Territory names from the `area_name` field. Multi-state events were kept as they are.
5. **Durations:** Kept the original duration field. Invalid negative values were flagged and left out of duration calculations.

## Key Findings

- **920 events** were recorded. The peak year was **2018** with 134 events. The count then fell to 63 in 2025.
- **Jammu and Kashmir** has the most shutdown-state records (488), followed by Rajasthan (83), Manipur (75), and Haryana (45).
- The **median** shutdown lasted **2 days**, but the **average** was about **6.6 days**. The longest lasted 551 days.
- **Most common recorded causes:** political instability (216), protests (212), and communal violence (177). Together they make up about 66% of records.
- **Networks:** mobile connectivity was affected in about 97% of records. About 95% of records are full shutdowns rather than throttling.

> These are descriptive patterns in the recorded data. The analysis does not show why a shutdown was ordered or whether it worked.

## Challenges and Learnings

- **Messy locations:** The `area_name` field mixes cities, districts, regions, and multi-state descriptions. State counts are therefore shown as shutdown-state records, not unique events.
- **Skewed durations:** A few very long shutdowns pull the average up, so the dashboard shows the median as well.
- **Incomplete data:** Some records lack enough information to calculate a duration. These were flagged instead of estimated.
- **Recorded cause is not proof:** A cause in the dataset is what the source records. It is not proof that a shutdown was necessary or effective.
- **Open item:** For 2025, the cleaned data has 63 events, while Access Now's 2025 report says 65. The exact dataset version still needs to be documented and the gap checked.

## Data Source

- **Primary:** [Access Now STOP dataset](https://www.accessnow.org/shutdown-tracker/) (2016–2025)
- **Supporting:** [SFLC.in Internet Shutdown Tracker](https://internetshutdowns.in/), used for Indian context and checking records


Kajal · GitHub: [@Kajal429](https://github.com/Kajal429)

