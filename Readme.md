# PRODIGY_DS_05

## Objective
Analyze traffic accident data to identify patterns related to road conditions, weather, and time of day, and visualize accident hotspots and contributing factors, using the US Accidents (2016–2023) dataset.

---

## 📁 Project Structure

```
PRODIGY_DS_05/
│
├── US_Accidents_March23.csv                       # Dataset
├── task5_clean.csv                                # Cleaned dataset (not tracked in git)
├── Task_05.ipynb                                  # Main Python notebook
├── assets/                                        # Exported chart images
│   ├── time_patterns.png
│   ├── weather.png
│   ├── weather_impact.png
│   ├── road_condt.png
│   ├── correlation.png
│   ├── feature_importance.png
│   ├── permutation_feature_importance.png
│   ├── accident_hotspots.html
│   └── state_choropleth.html
└── README.md
```

---

## 📂 Dataset

**Source:** Kaggle

**Dataset Link:** https://www.kaggle.com/datasets/sobhanmoosavi/us-accidents

---

## Tools & Libraries
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Folium
- Plotly
- Scikit-learn
- Jupyter Notebook

---

## Key Tasks Performed
- Loaded the full US Accidents dataset (7,728,394 records, 46 columns) and trimmed it to 30 analysis-relevant columns, cutting memory usage from 3.6 GB to 1.5 GB
- Cleaned missing values using regional imputation — grouping by `State` before filling weather columns (`Temperature`, `Humidity`, `Pressure`, `Visibility`, `Wind_Speed`) with the median, rather than a single global fill
- Engineered time-based features from `Start_Time`: `Hour`, `DayOfWeek`, `Month`, `Time_of_Day` buckets (Morning/Afternoon/Evening/Night), and `Is_Weekend`
- Analyzed **time-of-day patterns**: accident frequency by hour, day of week, and month, surfacing rush-hour peaks and seasonal trends
- Analyzed **weather impact**: top weather conditions during accidents, and severity distribution against visibility, temperature, and precipitation
- Analyzed **road condition impact**: compared accident rate and average severity across 13 road-infrastructure features (`Junction`, `Traffic_Signal`, `Crossing`, `Railway`, etc.)
- Visualized **accident hotspots** using a Folium heatmap (100K-point sample) and identified the top 15 highest-accident cities (led by Houston, Miami, and Los Angeles)
- Mapped **state-level accident density** with a Plotly choropleth
- Quantified **contributing factors** with a correlation heatmap of weather variables against severity, followed by both Random Forest feature importance and permutation importance to cross-validate which factors most influence severity
- Summarized key findings on when, where, and under what conditions accidents are most frequent and most severe

---

**Rajvardhan Chachad**  
GitHub: [@rajchachad17](https://github.com/rajchachad17)
