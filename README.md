# 🚲 GeoBikeLLM: LLM-Powered Bike Route Planning with Air Quality and Vegetation-Aware Geospatial Intelligence

**GeoBikeLLM** is an intelligent route planning system for cyclists in **Chicago, Illinois**, that combines **Large Language Models (LLMs)**, **environmental datasets** (Air Quality, NDVI), and **OpenStreetMap (OSM)** bike infrastructure. It allows users to input trip requests in natural language, choose their environmental preferences (healthier or greener routes), and receive optimized bike paths with map visualizations and explanations.

---

## 🔍 Features

- ✅ **Natural Language Query Interpretation** using LLaMA 3.1 8B
- ✅ **Slider-Based Preference Input** for:
  - Air Quality Penalty (α)
  - Greenness Reward (β)
- ✅ **Environmental-Aware Pathfinding** using PM2.5 and NDVI
- ✅ **Shortest & Healthiest Route Recommendation** with trade-off control
- ✅ **Interactive Route Map** with ETA and start/end markers
- ✅ **Concise Route Explanations** via LLaMA 3.3 70B

---

## 🗂️ Repository Structure
```bash
fds-project-geollms/
├── Datasets/                        # PM2.5, NDVI, and OSM-based network data
├── AQ_Path_Selection/               # Pathfinding logic and algorithms
├── Visualization/                   # Heatmaps and system diagrams
├── literature/                      # Related research literature
├── Interface.ipynb                  # Gradio-based UI implementation
├── LLM_integration.ipynb            # LLM parsing and explanation logic
├── AQI_Dataset_Preprocessing.ipynb  # Data preprocessing and cleaning
├── Testing_Prompts.xlsx             # 35 prompt-based test cases
├── GeoBikeLLM Paper.docx            # Project methodology and write-up
└── README.md                        # Project documentation
```


---

## 🧪 LLM Integration and Evaluation

### 1. **Query Interpretation with LLaMA 3.1 8B**
- **Purpose**: Extracts origin, destination, and routing preference from free-form text
- **Evaluation**: 35 user prompts tested
- ✅ Origin/Destination Accuracy: 94.3% (33/35)
- ✅ Preference Accuracy: 94.3% (33/35)

### 2. **Explanation Generation with LLaMA 3.3 70B**
- **Purpose**: Generates natural language explanations for the chosen route
- **Evaluation**: Consistently aligned explanations based on slider inputs (α, β)

---

## 📊 Datasets

| Dataset         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| PM2.5 AQ Data   | Sensor-based air quality data across Chicago from the Eclipse AQ dataset   |
| NDVI Data       | Normalized Difference Vegetation Index values from satellite imagery       |
| OSM Network     | Bicycle infrastructure data from OpenStreetMap (Chicago-specific)          |

Each dataset is used in spatial weighting of the graph edges and visualized using Folium.

---

## 🚀 Getting Started

Follow the steps below to run the notebook interface and enable LLM-powered routing with Groq.

---

### 🔹 Step 1: Clone the Repository

```bash
git clone https://github.com/Dr-Isam-ALJAWARNEH/fds-project-geollms.git
cd fds-project-geollms
```
---

### 🔹 Step 2: Install Required Libraries
pip install gradio pandas networkx scipy folium geopy openai


---

### 🔹 Step 3: Get Your Groq API Key

1. Go to: https://console.groq.com  
2. Log in or sign up  
3. Create a new API key  

---

### 🔹 Step 4: Add Your API Key in the Notebook

In the `Interface.ipynb` file, locate the following line:

client = Groq(api_key="YOUR_GROQ_API_KEY")


Replace `"YOUR_GROQ_API_KEY"` with your actual key.

---

### 🔹 Step 5: Run the Notebook


Then:
- Enter a natural language prompt (e.g., "Go from Loop to Hyde Park")
- Adjust the sliders for air quality and greenness
- Click the button to generate the route and explanation

---
Supervised by:
[Dr. Isam Al Jawarneh](https://isamaljawarneh.github.io/)
### ✅ Done by:

- **Menatalla Haggag U23103328**
- **Lubana Al Rayes U23103394**
- **Esraa Alhamid U24105438**
- **Sara Alshamsi U24102808** 

