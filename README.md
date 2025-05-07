# 🧠 LLMs Integration for GeoBikeLLM

This module integrates Large Language Models (LLMs) into the GeoBikeLLM system to enable natural language interaction and provide intelligent interpretation of user prompts for bike route planning within Chicago, Illinois. It extracts structured trip information (origin, destination) and generates human-readable explanations for routing decisions.

---

## 📌 Purpose

The LLMs serve two main purposes:

1. **Query Interpretation**  
   Automatically extract structured information (origin, destination) from unstructured, user-written prompts using LLaMA 3.1 8B Instant.

2. **Explanation Generation**  
   Provide concise, natural language justifications for the recommended route using LLaMA 3.3 70B Versatile.

---

## 🧪 Evaluation Summary

We tested the query interpretation module on **35 diverse user prompts**. The results:

- **Location Extraction Accuracy**: 94.3% (33/35 prompts)
- **Preference Extraction Accuracy** (prior to slider UI): 94.3% (33/35 prompts)

This high accuracy confirms the model’s robustness, although routing preferences are now selected via sliders for better user control.

---

## 🧰 Requirements
 
- Python 3.9+
- [Groq Python SDK](https://github.com/groq/groq-python) for LLM access
- `gradio`, `networkx`, `scipy`, `folium`, `pandas`, `geopy`
 
Install dependencies:
```bash
pip install groq gradio networkx scipy folium pandas geopy
