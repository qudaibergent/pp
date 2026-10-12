# Internet use in Kazakhstan and neighbouring countries

MYP Personal Project 2026: data analysis and visualisation using Python.

**Research question:** How fast did internet use grow in Kazakhstan, and how does it compare with Kyrgyzstan, Uzbekistan, Turkmenistan, Russia, China and the world average?

Data: World Bank indicator IT.NET.USER.ZS (see `data/README.md` for exactly how it was obtained). Tools: Python, pandas, Matplotlib, VS Code, Git and GitHub.

## How to run

1. Install Python 3.10 or newer and VS Code with the Python and Jupyter extensions.
2. In a terminal inside this folder:
   ```
   python -m venv .venv
   .venv\Scripts\activate        (Windows)   or   source .venv/bin/activate   (macOS, Linux)
   pip install -r requirements.txt
   ```
3. Open `internet_kz_analysis.ipynb` in VS Code, choose the `.venv` kernel and press **Run All**. The notebook creates `data/clean/` and `figures/`.

## Project structure

```
data/raw/        original series, one CSV per country (never edited)
data/clean/      cleaned long table and summary table (made by the notebook)
figures/         the six charts as PNG files
internet_kz_analysis.ipynb   loading, quality checks, cleaning, statistics, charts, conclusions
```

## What the analysis does

1. Loads seven raw series and checks rows, missing values, duplicates and impossible values.
2. Cleans the data: drops missing years, uses the window 2000 to 2024, and does not fill gaps.
3. Calculates levels, growth in percentage points and the first year each country passed 10%, 50% and 90%.
4. Draws six charts of four types: line (2), bar (2), scatter and histogram.

## Findings (numbers come from the notebook output)

- Kazakhstan started far behind the world average (0.7% against 6.7% in 2000) and was still behind in 2005 (3.0% against 15.6%).
- It overtook the world average between 2005 and 2010 (31.6% against 28.5% in 2010). It passed 10% in 2008, 50% in 2011 and 90% in 2021.
- The fastest year was 2011 (+19.0 percentage points), followed by 2010 (+13.4) and 2012 (+11.3).
- From 2010 to 2017 Kazakhstan grew by 44.8 percentage points, the most of the six countries (Kyrgyzstan 34.5, Uzbekistan 32.8, Russia 27.0, China 20.0, Turkmenistan 18.2).
- Russia also passed 50% in 2011, then China in 2015, Kyrgyzstan in 2017 and Uzbekistan in 2018. The world average passed 50% in 2019.
- In 2023 Kazakhstan (92.9%) was 25.5 points above the world average (67.4%). In 2024 the values were Russia 94.4, Kazakhstan 93.4, Kyrgyzstan 92.0, China 92.0 and Uzbekistan 89.5.

## Limitations

- Turkmenistan has no data after 2017 and the world series ends in 2023. Gaps are shown, not filled.
- Methods differ between countries and years. Large jumps may partly reflect a change in survey method (not verified).
- A percentage of the population does not show speed, price or quality of internet access.
- The data was copied from the FRED mirror, not directly from the World Bank API.

## Sources

- World Bank (2026) Individuals using the Internet (% of population), IT.NET.USER.ZS. https://data.worldbank.org/indicator/IT.NET.USER.ZS
- UK Government Analysis Function, Chart guidance. https://analysisfunction.civilservice.gov.uk/
- pandas documentation: https://pandas.pydata.org/docs/
- Matplotlib documentation: https://matplotlib.org/stable/
