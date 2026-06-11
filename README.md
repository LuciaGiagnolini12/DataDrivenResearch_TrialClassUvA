# Data-Driven Research in Digital Humanities
## Session materials — Television News Archive case study

**Institution**: University of Amsterdam — Media & Information Studies  
**Programme**: Bachelor Media & Information Studies  
**Level**: Second-year BA  

---

## About this repository

This repository contains the materials for a session on data-driven research methods in digital humanities. The session uses television news coverage of COVID-19 as a case study. The underlying data source is the [Internet Archive Television News Archive](https://archive.org/details/tv) — a continuously updated collection of broadcast television recordings from selected stations, searchable via closed captions.

The workflow: **research question → archive → data → operationalisation → analysis → interpretation → limits**.

Each step is demonstrated in practice, using two tools:
- **[GDELT Television Explorer](https://api.gdeltproject.org/api/v2/summary/summary?d=iatv&t=summary)** — browser-based exploration of the Internet Archive Television News Archive
- **Google Colab** — Python notebook for analysis that goes beyond what the browser allows

---

## Repository structure

```
├── notebook/
│   ├── DH_TV_News_Analysis.ipynb
│   ├── DH_TV_News_Analysis.pdf
│   └── README.md
├── data/
│   ├── results-corona.csv
│   ├── results-covid.csv
│   ├── results-coronaOrCovid.csv
│   ├── daily-new-confirmed-covid-19-deaths-per-million-people.csv
│   └── README.md
├── slides/
│   └── lecture_slides.pdf
├── bibliography.md
└── README.md
```


