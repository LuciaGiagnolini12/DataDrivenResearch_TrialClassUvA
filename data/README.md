# Data

This folder contains the datasets used in the session notebook.

---

## Television coverage data

Source: [GDELT Television Explorer](https://api.gdeltproject.org/api/v2/summary/summary?d=iatv&t=summary)  
Underlying archive: [Internet Archive Television News Archive](https://archive.org/details/tv)  
Metric: percentage of monitored airtime (15-second intervals) in which the keyword appeared in the closed captions  
Stations: Al Jazeera (ALJAZ), BBC News (BBCNEWS), Bloomberg (BLOOMBERG), CNN (CNN), C-SPAN (CSPAN), Deutsche Welle (DW), Fox News (FOXNEWS), RT (RT)  
Period: December 2019 – October 2024  
Downloaded: June 2026  

| File | Keyword | Notes |
|---|---|---|
| `results-corona.csv` | `coronavirus` | Dominant term in early 2020 |
| `results-covid.csv` | `covid` | Takes over from late 2020 |
| `results-coronaOrCovid.csv` | `coronavirus OR covid` | Combined — most complete picture of coverage |

**Important**: closed captions are produced by human stenographers in real time. Terms may be misspelled, abbreviated, or omitted. A zero result does not mean a topic was not discussed — it may mean the captioner used a different term.

---

## Epidemiological data

Source: [Our World in Data — COVID-19 deaths per million](https://ourworldindata.org/covid-deaths)  
Original source: WHO / Johns Hopkins University  
Geography: United States only  
Period: March 2020 – May 2026  

| File | Contents |
|---|---|
| `daily-new-confirmed-covid-19-deaths-per-million-people.csv` | Daily confirmed COVID-19 deaths per million people, United States |

**Note**: this dataset comes from a different institution, with a different methodology and a different object of measurement than the television coverage data. It is included to support cross-source comparison — asking not what the data shows in isolation, but where two independent datasets diverge and what that divergence might mean.

---

## Declared limits

- This archive covers primarily American and British national television — not global media, not local broadcasting, not non-English-language outlets
- Coverage reflects the scope of Internet Archive's monitoring infrastructure at the time of data collection
- The station selection intentionally includes broadcasters from outside the Anglo-American context — Al Jazeera (Qatar), Deutsche Welle (Germany), RT (Russia) — to allow limited comparative analysis. However, these stations have different editorial mandates, different audience bases, and different relationships to the events covered. They should not be treated as equivalent data points without accounting for those differences
- The datasets in this folder come from different sources, collected for different purposes, using different methodologies. Cross-source comparison is valid only when the differences between sources are made explicit and the claims are scoped accordingly
- As [Henrich, Heine and Norenzayan argued in 2010](https://doi.org/10.1038/466029a): most people are not WEIRD. Neither are most media systems. Findings from this archive describe a specific, geographically and linguistically situated slice of global media production
