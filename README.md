# Which EU Country is Leading the Green Transition?

![Image](https://github.com/user-attachments/assets/e55bd771-c594-4b4b-a134-ea961ded162b)

A multivariate Data Analysis project, examining sustainability performance across 27 EU member states over three time periods (2018, 2020, 2022), using Factor and Cluster Analysis to identify which countries are leading (and which are falling behind) Europe's green transition.

**Course:** Data Analysis 2025/2026 — Nova IMS, Universidade Nova de Lisboa

---

## Research Question

*Which European Union countries leading Europe's green transition, and which risk falling behind the EU's climate and sustainability targets?*

---

## Repository Contents

1. `projectguidelines` — course guidelines for the project
2. `WhichEUcountryGreenT.pdf` — final report
3. `ee25-originaldataindicators-data-csv.zip` — raw dataset downloaded from the EEA
4. `merged project data.xlsx` — cleaned and merged dataset used for analysis
5. `yearly_country_factor_scores.csv` — country factor scores produced by the Factor Analysis and used as input for clustering
6. `notebook1.ipynb` — Exploratory Data Analysis and Factor Analysis, by Pedro Salgado
7. `notebook2.ipynb` — Cluster Analysis, by Pedro Salgado and Pedro Ramalho
8. `teachersannotations` — teacher's improvement suggestions

---

## Data

- **Source:** [European Environment Agency (EEA)](https://www.eea.europa.eu/)
- **Scope:** All 27 EU member states across 2018, 2020 and 2022
- **Observations:** Each row represents a unique country–year pair (e.g., `Austria_2018`)
- **Variables (19):** Covering environmental pressures, energy systems, green economic structure, resource use, climate-related impacts and social inequality

| Variable | Description |
|---|---|
| `Consumption_Footprint` | Consumption-based environmental impacts |
| `Organic_Farming` | Sustainable agriculture share |
| `Re_used_Material` | Circular use of materials |
| `Climate_Losses` | Economic losses from climate-related events |
| `Eco_Innovation` | Eco-innovation performance index |
| `EGSS_Employment` | Employment in environmental goods & services sector |
| `EGSS_Output` | Output of environmental goods & services sector |
| `Energy_Poverty` | Energy vulnerability indicator |
| `Env_Protection_Expenditure` | Public environmental expenditure |
| `Env_Taxes` | Environmental taxation |
| `Final_Energy_Consumption` | Final energy demand |
| `Fossil_Fuel_Subsidies` | Fossil fuel support |
| `Air_Pollution_Health_Impact` | Health impacts of air pollution |
| `LULUCF_Emissions` | Land-use related emissions |
| `Renewable_Energy_Share` | Renewable energy penetration |
| `Protected_Area_Share` | Biodiversity protection efforts |
| `GHG_Emissions` | Greenhouse gas emissions |
| `Waste_Generation` | Waste generation |
| `Gini_Coefficient` | Income inequality |

---

## Methodology
```
1. **Data Collection** — EEA official dataset, 19 sustainability indicators across 27 EU member states
2. **Data Preprocessing** — data integration, cleaning and missing value treatment in Excel and Python
3. **Exploratory Data Analysis** — univariate and bivariate analysis to characterise distributions and relationships
4. **Factor Analysis** — dimensionality reduction to three latent factors; factor scores saved to `yearly_country_factor_scores.csv`
5. **Cluster Analysis** — country grouping based on factor scores to identify sustainability profiles
```

Full detail in [`WhichEUcountryGreenT.pdf`](./WhichEUcountryGreenT.pdf).

---

## Key Findings

Three latent factors emerged from the analysis — **Eco-Innovation & Green Industry (EIGI)**, **Social Equity & Energy Vulnerability (SEEV)** and **Clean Environment & Ecosystem Protection (CEEP)** — which were used to cluster all 27 member states into four distinct sustainability profiles.

<img width="754" height="758" alt="Image" src="https://github.com/user-attachments/assets/89d807db-3349-45c7-bbbc-832249e2f0e4" />

**Cluster 1 — Sustainability Lagging Countries**  
Belgium, Croatia, Czechia, France, Germany, Hungary, Ireland, Italy, Malta, Netherlands, Poland, Romania, Slovakia, Slovenia, Spain

**Cluster 2 — Energy-Vulnerable and Unequal Countries**  
Bulgaria, Cyprus, Greece, Lithuania, Portugal

**Cluster 3 — Environmental Quality Leaders**  
Denmark, Latvia, Sweden

**Cluster 4 — Green Economic and Innovation Leaders**  
Austria, Estonia, Finland, Luxembourg


<img width="1390" height="523" alt="Image" src="https://github.com/user-attachments/assets/c2580c60-e036-4659-b087-da1ee4f45fa4" />




---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis language |
| Jupyter Notebook | Interactive computing (VS Code + Google Colab) |
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `scikit-learn` | Preprocessing, PCA, clustering |
| `matplotlib` / `seaborn` | Visualisation |
| `factor_analyzer` | Factor Analysis, KMO, Bartlett's test, rotation |
| `pingouin` | Statistical testing |
| Microsoft Excel | Initial data cleaning and integration |

---

## Report

Full methodology, results and discussion are in [`WhichEUcountryGreenT.pdf`](./WhichEUcountryGreenT.pdf).

---

## Data Source

European Environment Agency (EEA). *EEA Indicators Dataset (EE25)*. [https://www.eea.europa.eu](https://www.eea.europa.eu).

---

*Nova IMS — Universidade Nova de Lisboa | Data Analysis 2025/2026*
