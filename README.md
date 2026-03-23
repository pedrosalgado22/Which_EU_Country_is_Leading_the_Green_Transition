# 🌿 Which EU Country is Leading the Green Transition?

> A multivariate data analysis project examining sustainability performance across 27 EU member states over three time periods (2018, 2020, 2022), using Factor Analysis and Cluster Analysis to identify which countries are leading — and which are falling behind — Europe's green transition.

**Course:** Data Analysis 2025/2026 — Nova IMS, Universidade Nova de Lisboa  
**Authors:** Pedro Salgado · Pedro Ramalho  
**Instructors:** Frederico Cruz Jesus · Maria Inês Monteiro  

---

## 📌 Research Question

*Which European Union countries are best positioned to lead the green transition, and which risk falling behind the EU's climate and sustainability targets?*

---

## 📁 Repository Structure

```
Which_EU_Country_is_Leading_the_Green_Transition/
│
├── projectguidelines              # Nova IMS course guidelines for the project
├── WhichEUcountryGreenT.pdf       # Final project report
│
├── ee25-originaldataindicators-data-csv.zip   # Raw data downloaded from EEA
├── merged project data.xlsx                   # Cleaned and merged dataset for analysis
├── yearly_country_factor_scores.csv           # Factor scores output from Factor Analysis
│
├── notebook1.ipynb                # Exploratory Data Analysis + Factor Analysis (Pedro Salgado)
└── notebook2.ipynb                # Cluster Analysis (Pedro Salgado & Pedro Ramalho)
```

---

## 🗃️ Data

- **Source:** [European Environment Agency (EEA)](https://www.eea.europa.eu/) — official EU agency
- **Raw file:** `ee25-originaldataindicators-data-csv.zip`
- **Scope:** All 27 EU member states across three time frames — **2018, 2020, and 2022**
- **Observations:** Each row represents a unique country–year pair (e.g., `Austria_2018`)
- **Variables (19):** Covering environmental pressures, energy systems, green economic structure, resource use, climate-related impacts and social inequality:

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

## 🔬 Methodology

### 1. Data Preprocessing
- Data integration, cleaning and missing value treatment performed in **Microsoft Excel** and **Python**
- Outlier exploration and variable standardisation performed prior to multivariate analysis
- Final cleaned dataset stored in `merged project data.xlsx`

### 2. Exploratory Data Analysis (EDA)
- Univariate and bivariate analysis to characterise distributions and relationships
- Performed in `notebook1.ipynb`

### 3. Factor Analysis (FA)
- **Bartlett's Test of Sphericity** and **KMO measure** used to validate FA applicability
- **Principal Component Analysis (PCA)** applied to determine the number of factors to retain
- **Factor rotation** applied to maximise interpretability
- Three latent factors identified and extracted, with scores saved to `yearly_country_factor_scores.csv`
- Performed in `notebook1.ipynb`

### 4. Cluster Analysis
- Country–year factor scores used as input
- Cluster structure determined and interpreted in terms of green transition positioning
- Performed in `notebook2.ipynb`

---

## 📊 Key Findings

Factor Analysis reduced the 19 variables to **three interpretable latent dimensions**:

| Factor | Label | Key Variables |
|---|---|---|
| **F1** | Eco-Innovation & Green Industry (EIGI) | EGSS Employment, EGSS Output, Eco-Innovation, Organic Farming |
| **F2** | Social Equity & Energy Vulnerability (SEEV) | Energy Poverty, Fossil Fuel Subsidies, infrastructural inefficiency |
| **F3** | Clean Environment & Ecosystem Protection (CEEP) | Renewable Energy Share, Air Pollution Health Impact, Protected Area Share |

Cluster Analysis revealed a **clear geographical divide** across EU member states:

- 🟢 **Frontrunners** — Nordic and Baltic countries, Austria and Luxembourg: consistently strong across all three factors, combining advanced eco-innovation, low energy vulnerability and high environmental quality.
- 🟡 **Mixed performers** — Major economies (Germany, France, Netherlands, Spain, Italy, Poland): solid in some dimensions but structural challenges remain; collectively the largest absolute emitters.
- 🔴 **Laggards** — Southern and Eastern European economies: higher energy poverty, inequality and fossil fuel dependency constrain progress despite visible renewable energy efforts.

> The results suggest the socioeconomic divide within Europe propagates directly into sustainability performance, making coordinated EU-level support for vulnerable regions — not just national-level ambition — essential for a genuine continental green transition.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python 3 | Core analysis language |
| Jupyter Notebook | Interactive computing environment (VS Code + Google Colab) |
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `scikit-learn` | Preprocessing, PCA, clustering |
| `matplotlib` / `seaborn` | Data visualisation |
| `factor_analyzer` | Factor Analysis, KMO, Bartlett's test, rotation |
| `pingouin` | Statistical testing |
| Microsoft Excel | Initial data cleaning and integration |

---

## 📄 Report

The full report — including methodology detail, all results, discussion and conclusions — is available in [`WhichEUcountryGreenT.pdf`](./WhichEUcountryGreenT.pdf).

---

## 📚 Data Source

> European Environment Agency (EEA). *EEA Signals — Environmental Indicators Dataset (EE25)*. Retrieved from [https://www.eea.europa.eu](https://www.eea.europa.eu).

---

*Nova IMS — Universidade Nova de Lisboa | Data Analysis 2025/2026*
