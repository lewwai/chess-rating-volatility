# Chess Rating Volatility Analysis

An exploratory analysis of how age, activity, and the FIDE K-factor relate to monthly chess rating changes. This group project was completed for DSA2101 at the National University of Singapore.

The analysis matches August and September 2025 FIDE rating records and focuses on **37,533 active players** who played at least one game in September.

## Explore the project

- [Analysis notebook](chess_rating.ipynb): Python code, explanations, and saved outputs.
- [Interactive report](Chess_Rating_Analysis.html): download the HTML file and open it in a browser. Figure 1 includes a dropdown for all active players and players who played exactly seven games. The report embeds its chart assets and works offline.

GitHub's notebook preview is static. Use the HTML report to explore the interactive chart.

## Approach

1. Inspect the two monthly datasets for duplicate identifiers and data quality issues.
2. Match players using both ID and name to avoid incorrect matches from duplicated IDs.
3. Calculate rating changes and derive age, age-group, and starting-rating variables.
4. Restrict the analysis to active players and compare rating-change distributions using Plotly and Matplotlib/Seaborn visualisations.

The report explores wider rating changes among younger players, whether that pattern persists among players with the same recorded activity, and how K-factor categories relate to the observed distributions.

## Run the notebook

Use Python 3 and install the dependencies:

```bash
python -m pip install -r requirements.txt
jupyter notebook chess_rating.ipynb
```

Run the cells in order. The notebook downloads the source CSVs directly from TidyTuesday, so executing it requires an internet connection. Google Colab is another option for running the notebook.

The Python package versions are not pinned to the original coursework environment. The HTML report provides a saved view of the submitted analysis.

## Data and limitations

Data: [TidyTuesday's FIDE chess player ratings dataset](https://github.com/rfordatascience/tidytuesday/tree/main/data/2025/2025-09-23), originally sourced from [FIDE](https://ratings.fide.com/).

The project examines one transition between two monthly rating lists. Here, "volatility" refers to the spread of observed monthly rating changes, rather than a long-term volatility estimate for each player. The analysis is exploratory and does not establish causal effects of age, activity, or K-factor. The coursework analysis and its interpretations are retained in the report.

## Team

Eng Cheng Xin, Koh Lin Kiat, Lew Wai Loon, Wong E Shen, and Zhou Qian Li.

Full references and individual contributions appear in the notebook and report.
