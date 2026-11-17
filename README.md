# Global Tuberculosis Data — Analysis & Visualization

Data Analysis & Visualization (DAV) course project exploring WHO tuberculosis data — TB case notifications, TB/HIV and treatment outcomes by country, region and year — with a set of interactive **D3.js** charts.

> Team: Maaz (22i-1873), Hashir Ahmed (22i-1988), Azhaff Khalid (22i-1895) — DS-A.

## Data

| File | Contents |
|---|---|
| `tb_2022-09-30.csv` | TB case notifications by country and year |
| `tbhiv_2022-09-27.csv` | TB/HIV indicators |
| `tx_2022-08-29.csv` | Treatment outcomes |
| `longitude-latitude.csv` | Country coordinates |
| `final_cleaned_data_v2.csv`, `preprocessed_data_for_visualization.csv`, `Merged_Data_with_Latitude_and_Longitude.csv` | Cleaned / merged outputs |

## Pipeline

`preprocessed_data.ipynb` merges the three datasets, drops columns with more than 50% missing values, cleans the rest, joins country coordinates and exports JSON for each chart.

## Visualizations (`d3/`)

| Page | Chart |
|---|---|
| `dashboard.html` | Dashboard linking the charts |
| `mapchart.html` | Geographic map of TB cases |
| `bubblegraph.html` | Animated bubble chart over time |
| `forcedirected.html` | Force-directed network of countries and regions |
| `sunburst.html` | Sunburst by WHO region → country |
| `treemap.html` | Hierarchical tree map |

## View the charts

The pages load JSON files, so serve the folder instead of double-clicking the HTML:

```bash
cd d3
python -m http.server 8000
```

Then open http://localhost:8000/dashboard.html.

The full write-up is in `Report.pdf`.
