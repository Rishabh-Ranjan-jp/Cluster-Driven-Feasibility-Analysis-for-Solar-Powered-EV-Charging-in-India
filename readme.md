# Cluster‑Driven Feasibility Analysis for Solar‑Powered EV Charging in India

🚗🔋☀️  
**A data‑driven roadmap to prioritize Indian states for solar EV charging infrastructure**, balancing solar potential, EV growth, and infrastructure readiness.

---

## 📌 Project Objective

To identify the most promising Indian states for deploying **solar‑powered EV charging infrastructure** using a clustering-based approach, helping stakeholders optimize investments across **feasibility** and **readiness** dimensions.

---

## 🔍 Key Questions

1. **Feasibility**: Which states combine high solar potential with rapid EV adoption?
2. **Readiness**: Among those, which states already have supportive infrastructure and urban density?
3. **Strategy**: How should deployment efforts be tailored—pilot programs or rapid expansion?

---

## 📊 Datasets Used

| Category             | Source                                                       |
|----------------------|--------------------------------------------------------------|
| Solar Irradiance     | [Global Solar Atlas](https://globalsolaratlas.info/download/india) |
| EV Registrations     | [VAHAN Dashboard](https://vahan.parivahan.gov.in/vahan4dashboard) |
| Population Data      | [Census India 2011](https://censusindia.gov.in/)             |
| Charging Infrastructure | [PIB PDF Report](https://pib.gov.in/PressReleaseIframePage.aspx?PRID=2003003) |

*Additional details on collection, cleaning, and preprocessing available in the notebook.*

---

## 🧮 Methodology

### Phase 1: Feasibility Clustering
- **Features**: EV growth rate, solar irradiance  
- **Model**: Gaussian Mixture Model (k=2)  
- **Output**: High vs. Low Feasibility states  

### Phase 2: Readiness Clustering
- **Features**: EVs per million, stations per million, urbanization ratio  
- **Model**: K-Means Clustering (k=2)  
- **Output**: High vs. Low Readiness states  

### Phase 3: Strategy Assignment
Combining both cluster labels into a 2×2 strategy matrix:

| Readiness \ Feasibility | Low Feasibility               | High Feasibility              |
|--------------------------|-------------------------------|-------------------------------|
| **Low Readiness**        | Gradual Infrastructure Build | —                             |
| **High Readiness**       | —                             | Immediate Solar EV Expansion |

---

## 🗺️ Key Insights

### 🌟 Top Strategy States  
| State | EVs per Million | Solar Irradiance (kWh/m²) |
|-------|------------------|---------------------------|
| Goa   | 6,501            | 1,892.9                   |
| Delhi | 4,389.6          | 1,726.4                   |

### 🚧 Bottom States  
Low EV adoption despite high solar potential—e.g., Telangana, Nagaland.

---

## 📈 Visualizations

- 📊 Bar chart: States per deployment strategy  
- 📉 Grouped bar: Avg EVs/million & solar potential by strategy  
- 🫧 Bubble plot: Solar vs. EVs/million (bubble ∝ population)  
- 📌 Horizontal bar: Top 5 vs. bottom 5 state comparison  

---

## 🧭 Next Steps

1. **Policy Review**: Qualitative analysis of top/bottom states  
2. **Enhanced Modeling**: Add cloud cover, land-use constraints  
3. **Pilot Design**: Smart solar charging hubs in Goa & Delhi  
4. **Awareness Campaigns**: Micro-pilots in low-uptake, high-potential states

---

## 🧠 Tech Stack

- Python 🐍  
- pandas, scikit-learn, seaborn, matplotlib  
- Jupyter Notebook (Modular & Clean Structure)  

---

## 📁 Repo Structure

```
├── datasets/                            # Raw and merged datasets  
│   ├── raw/                             # Original data files  
│   │   ├── 2011-IndiaState-0000.xlsx    # Data for India state-level 2011 info  
│   │   ├── operationalChargers.csv      # Data on operational EV chargers  
│   │   ├── state_solar_irradiance.csv  # Solar irradiance data by state  
│   │   ├── statewiseev2020.xlsx         # EV data from 2020  
│   │   ├── statewiseev2023.xlsx         # EV data from 2023  
│   │   ├── statewisepop.xlsx           # Statewise population data  
│   │   ├── mergeddata.xlsx             # Merged raw data (pre-cleaning)  
├── 'Cluster-Driven Feasibility Analysis for Solar-Powered EV Charging in India.ipynb'  # Jupyter Notebook  
├── readme.md                            # Project overview

```

---

## 👤 Author

**Rishabh Ranjan**  
EduNet Workshop, 2025  
[GitHub Profile](https://github.com/Rishabh-Ranjan-jp)

---

## 📎 Repository

```bash
git clone git@github.com:Rishabh-Ranjan-jp/Cluster-Driven-Feasibility-Analysis-for-Solar-Powered-EV-Charging-in-India.git
```

--- 
