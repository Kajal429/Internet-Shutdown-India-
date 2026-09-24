Internet Shutdowns in India (2016–2025)
link:https://app.powerbi.com/links/m205wXRizt?ctid=4517da72-c8f7-4cec-b2fc-fda9fe4354f9&pbi_source=linkShare
A data project that cleans, analyzes, and visualizes 920 recorded internet shutdown events in India. It uses Python for cleaning, SQL for analysis, and Power BI for an interactive dashboard.

The full write-up is in the case study document: Internet Shutdowns in India: Balancing Public Safety and Digital Rights.

Why this project exists

The Indian government does not keep one central record of internet shutdown orders issued by states and Union Territories. Police and public order are State subjects, so the Department of Telecommunications does not maintain them centrally. That makes shutdowns hard to compare.

This project uses public data from researchers and civil-society groups to answer one question:

What patterns can be observed in internet shutdowns in India in terms of frequency, duration, location, reported reason, and network type?

What I found
920 shutdown events were recorded from 2016 to 2025.
The peak year was 2018 with 134 events. The lowest recent year in this dataset is 2025 with 63.
Jammu and Kashmir has the most shutdown-state records (488), followed by Rajasthan (83) and Manipur (75).
The median shutdown lasted 2 days, but the average was about 6.6 days. A few very long shutdowns (up to 551 days) pull the average up.
The most common recorded causes are political instability (216), protests (212), and communal violence (177).
Mobile networks were affected in about 97% of records.

These are descriptions of the recorded data. They do not prove why a shutdown happened or whether it worked.

Data sources
Source	How it is used
Access Now STOP dataset	Main dataset (2016–2025)
SFLC.in Internet Shutdown Tracker	Supporting source for Indian context and checking records

Dashboard
The Power BI dashboard is one page.

Key numbers: total shutdowns, median duration, number of affected states and Union Territories, longest shutdown.
Charts: shutdowns by year, by state, duration, reported cause, network, and restriction type.
Filters: year, state or Union Territory, cause, network, restriction type.
Things to keep in mind
The data is not a complete government record. Some shutdowns may be missing.
State counts show shutdown-state records, not unique events, because some events affect more than one state.
Some durations are missing or invalid, so duration results use only usable records.
A recorded cause is what the source says. It is not proof that the shutdown was necessary or effective.
For 2025, my cleaned data has 63 events, while Access Now's 2025 report says 65. I still need to record the exact dataset version and look into this gap.
