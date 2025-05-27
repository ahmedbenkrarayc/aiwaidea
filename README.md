# 🏥 MediMate – AI Health Companion

## 🔍 Overview

**MediMate** is a Python-based AI agent designed to help users understand their symptoms using natural language input. The agent analyzes described symptoms, matches them with a lightweight symptom-condition database, and provides possible causes along with actionable advice (e.g., rest, hydration, or a recommendation to consult a doctor).  
This project is beginner-friendly and focuses on the practical use of AI agents without relying on complex machine learning models.

---

## 🚀 Features

- 🤖 **AI Symptom Checker**: Understands natural language inputs about health symptoms.
- 📚 **Symptom-to-Condition Matching**: Uses a simple dataset to suggest possible causes.
- 💬 **Friendly Health Advice**: Provides self-care tips and red flag alerts when needed.
- 📆 **Symptom Tracking (Optional)**: Remembers previous entries with timestamps.
- 🌿 **Wellness Tips Generator (Optional)**: Offers daily or situational health suggestions.

---

## ⚙️ Tech Stack

| Layer           | Tools                                      |
|----------------|---------------------------------------------|
| Language        | Python                                     |
| AI/NLP          | OpenAI API (or any LLM), prompt engineering |
| Backend         | Flask or FastAPI                           |
| Agent Framework | LangChain (optional, for tool-based agents)|
| UI              | Streamlit, simple Flask web UI             |
| Storage         | JSON or SQLite (for optional tracking)     |

---

## 🧠 AI Agent Behavior

- **Input**: `"I feel tired, with a sore throat and mild fever."`
- **Process**:
  - Parses symptoms using GPT or regex.
  - Matches them with entries in a dataset.
  - Determines possible conditions (not diagnosis).
  - Provides a helpful and human-like response.
- **Output**:
  > "It seems you may have symptoms similar to a cold or mild flu. Make sure to rest, drink plenty of fluids, and monitor your temperature. If the fever persists for more than 3 days, consider consulting a doctor."

---

## 📂 Dataset Sources (Free & Public)

You can use or adapt datasets from the following sources:

1. **GitHub: Symptom-Disease Datasets**
   - [kaushikj/symptom-disease-dataset](https://github.com/kaushikj/symptom-disease-dataset)
   - [abavala/disease-symptoms-dataset](https://github.com/abavala/disease-symptoms-dataset)

2. **Kaggle:**
   - Search: ["symptom disease dataset"](https://www.kaggle.com/search?q=symptom+disease+dataset)

3. **Public Health Websites (Scraping or Manual)**
   - [NHS Conditions](https://www.nhs.uk/conditions/)
   - [Mayo Clinic Symptoms](https://www.mayoclinic.org/symptoms)

4. **Example Custom Dataset**
```json
{
  "fever, sore throat, fatigue": ["flu", "common cold", "COVID-19"],
  "nausea, headache": ["migraine", "food poisoning", "dehydration"],
  "chest pain, shortness of breath": ["panic attack", "heart condition"]
}
