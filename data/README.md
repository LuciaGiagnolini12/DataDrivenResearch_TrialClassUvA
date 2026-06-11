Fammi leggere i file per darti info precise.Perfetto — ho tutto. Ecco il README dei dati con le descrizioni complete:

---

```markdown
# Data

This folder contains the datasets used in the session notebook.

---

## Television coverage data

Source: [GDELT Television Explorer](https://api.gdeltproject.org/api/v2/summary/summary?d=iatv&t=summary)  
Underlying archive: [Internet Archive Television News Archive](https://archive.org/details/tv)  
Exported via: GDELT Volume Timeline — Export → CSV  
Stations: Al Jazeera (ALJAZ), BBC News (BBCNEWS), Bloomberg (BLOOMBERG), CNN (CNN), C-SPAN (CSPAN), Deutsche Welle (DW), Fox News (FOXNEWS), RT (RT)  
Period: December 2019 – October 2024  
Downloaded: June 2026  

### File structure

Each file has 472 rows and 3 columns:

| Column | Format | Description |
|---|---|---|
| `Date` | `MM/YYYY` | Month of broadcast |
| `Series` | string | Station identifier |
| `Value` | float | Percentage of 15-second intervals in which the keyword appeared in the closed captions, for that station in that month |

A value of `0.0` means the keyword did not appear in any monitored caption for that station in that month. It does not necessarily mean the topic was not discussed — the captioner may have used a different term, or the term may have been omitted under time pressure.

### Files

| File | Query | Peak value | Notes |
|---|---|---|---|
| `results-corona.csv` | `coronavirus` | 11.05% (BBC News, March 2020) | Dominant term in early 2020; declines as terminology shifts |
| `results-covid.csv` | `covid` | 6.11% (CNN, April 2021) | Takes over from late 2020 onwards |
| `results-coronaOrCovid.csv` | `coronavirus OR covid` | 13.94% (BBC News, March 2020) | Combined query — most complete picture of total coverage |

These three files come from the same underlying archive and the same GDELT interface, queried with different keywords. They are intended to be read in sequence: the shift from `results-corona.csv` to `results-covid.csv` illustrates the operationalisation problem — the terminology changed, not the coverage.

---

## Epidemiological data

Source: [Our World in Data — COVID-19 deaths per million](https://ourworldindata.org/covid-deaths)  
Original source: WHO / Johns Hopkins University  
Geography: United States only  
Period: March 2020 – May 2026  

### File structure

`daily-new-confirmed-covid-19-deaths-per-million-people.csv` has 2,269 rows and 4 columns:

| Column | Format | Description |
|---|---|---|
| `Entity` | string | Country name (`United States`) |
| `Code` | string | ISO country code (`USA`) |
| `Day` | `YYYY-MM-DD` | Date |
| `New deaths (per 1M)` | float | Daily confirmed COVID-19 deaths per million people |

This dataset is included not to measure television coverage, but to provide an independent reference point from a different source, institution, and methodology. It enables cross-source comparison: where do the two datasets diverge, and what might explain that divergence?

---

## Declared limits

- This archive covers primarily American and British national television — not global media, not local broadcasting, not non-English-language outlets
- Coverage reflects the scope of Internet Archive's monitoring infrastructure at the time of data collection
- The station selection intentionally includes broadcasters from outside the Anglo-American context — Al Jazeera (Qatar), Deutsche Welle (Germany), RT (Russia) — to allow limited comparative analysis. However, these stations have different editorial mandates, different audience bases, and different relationships to the events covered. They should not be treated as equivalent data points without accounting for those differences
- The datasets in this folder come from different sources, collected for different purposes, using different methodologies. Cross-source comparison is valid only when the differences between sources are made explicit and the claims are scoped accordingly
- As [Henrich, Heine and Norenzayan argued in 2010](https://doi.org/10.1038/466029a): most people are not WEIRD. Neither are most media systems. Findings from this archive describe a specific, geographically and linguistically situated slice of global media production
```
