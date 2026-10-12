# Data provenance

**Indicator:** Individuals using the Internet (% of population), World Bank code IT.NET.USER.ZS, World Development Indicators. Original source of the numbers: International Telecommunication Union, reported through the World Bank.

**How the files were obtained:** the series were copied on 12 October 2026 from the FRED pages that republish the World Bank series (https://fred.stlouisfed.org/data/ITNETUSERP2KAZ and the same address with KGZ, UZB, TKM, RUS, CHN, WLD). The World Bank API itself could not be reached from the environment where the data was collected. Nothing was edited by hand. A "." in the FRED table is stored as an empty value.

| File | Series ID | Years | Last updated on FRED |
|---|---|---|---|
| raw/KAZ.csv | ITNETUSERP2KAZ | 1990 to 2024 | 2025-10-08 |
| raw/KGZ.csv | ITNETUSERP2KGZ | 1990 to 2024 | 2026-04-14 |
| raw/UZB.csv | ITNETUSERP2UZB | 1990 to 2024 | 2026-04-14 |
| raw/TKM.csv | ITNETUSERP2TKM | 1990 to 2017 | 2025-10-08 |
| raw/RUS.csv | ITNETUSERP2RUS | 1990 to 2024 | 2026-04-14 |
| raw/CHN.csv | ITNETUSERP2CHN | 1990 to 2025 | 2026-04-14 |
| raw/WLD.csv | ITNETUSERP2WLD | 1990 to 2023 | 2024-09-19 |

Some raw files hold values rounded to 6 decimals (KAZ, TKM) and others hold more digits. This does not affect the analysis, which rounds to 2 decimals.

`clean/` is created by the notebook. Do not edit it by hand.

**Check to do:** compare a few values with https://data.worldbank.org/indicator/IT.NET.USER.ZS (for example Kazakhstan 2024) once the World Bank site is reachable, and note the result in the project journal.
