# CollabSearch: LLaMA as Collaborative Agent for Search Tasks

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Contributions](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)



A novel search framework that transforms single-turn LLM interactions into structured, multi-stage collaborative processes. **CollabSearch** addresses query disambiguation challenges through user-guided clarification rather than probabilistic interpretation.

---

## 📌 Overview

CollabSearch implements an **Adaptive Role Playing Prompts (ARPP)** framework that extends the CoLA methodology through dynamic expert role generation. Rather than relying on static multi-agent systems, it simulates collaborative analysis within a single LLM using contextually appropriate expert personas.

---

## ✨ Key Features

### Core Frameworks
- **Dual-Intent Disambiguation System** → Two-stage user-guided clarification *(domain identification → answer-type selection)*  
- **Adaptive Role Playing Prompts (ARPP)** → Dynamic expert persona generation based on query context  
- **Smart Routing System** → Conditional framework activation based on query type  
- **RAG Enhancement Module** → Optional post-processing fact-checking with Google Search integration  

### Processing Pipeline
1. **Query Processing** — LLaMA-based topic identification  
2. **Disambiguation** — User-controlled domain clarification  
3. **Answer-Type Selection** — Personalized response format selection  
4. **Query Optimization** — REW methodology integration  
5. **Expert Analysis** — Multi-perspective synthesis  
6. **Smart Routing** — Conditional framework activation  
7. **Response Generation** — Tailored synthesis methods  
8. **RAG Enhancement** — Optional fact-checking with source verification  

---

<p align="center">
  <img src="Images/layered_architecture.jpg" alt="CollabSearch" width="400"/>
</p>
## ⚙️ Installation

### Prerequisites
```bash
pip install gradio langchain openai google-api-python-client pandas
```

### Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/collabsearch.git
cd collabsearch

# Run the system
python collabsearch_main.py
```

Configure **LLaMA 3.0-8B** access and Google Search API credentials before running.  

---

## 🚀 Usage

### Basic Query Processing
```python
from collabsearch import CollabSearchFramework

# Initialize framework
cs = CollabSearchFramework(model="llama-3.0-8b")

# Process query with disambiguation
result = cs.process_query(
    query="Latest iPhone models",
    enable_rag=True
)
```

### Answer Type Selection
The system provides **three main synthesis methods**:
- 🧩 **Decision-Making** → Reasoning-enhanced debating stage  
- 🛠️ **Solution-Focused** → Practical step-by-step guidance  
- 📚 **Informational** → Comprehensive information synthesis  

---

## 📊 Research Validation

Based on a **24-participant user study** comparing CollabSearch against baseline LLM systems:

| Metric                   | CollabSearch | Baseline | Improvement |
|---------------------------|--------------|----------|-------------|
| Intent Recognition        | 79.2%        | 65.4%    | **+13.8%** |
| Cognitive Load Reduction  | 27%          | -        | (via disambiguation) |
| User Preference           | 66.7%        | 33.3%    | **+33.4%** |
| Multi-perspective Analysis| 4.13/5       | 3.29/5   | **+0.84**  |

### Performance by Task Category
- **Disambiguation Tasks** → 100% success rate with perfect intent recognition  
- **Decision-Making** → Enhanced multi-perspective analysis with reasoning-enhanced debating  
- **Informational Tasks** → Improved comprehensiveness (+0.42 vs baseline)  
- **Procedural Tasks** → Better structured guidance (+0.62 vs baseline)  

---

## 🔧 Technical Implementation

### Core Components
- **LLaMA 3.0-8B** — Foundation model for text processing  
- **Gradio Interface** — Interactive web-based UI with state management  
- **Google Search API** — RAG enhancement & fact-checking  
- **REW Query Optimization** — Adaptive query reformulation  

### Smart Routing Logic
```python
def intelligent_routing(query_type):
    if query_type == "DECISION_MAKING":
        return activate_reasoning_debate_stage()
    elif query_type == "SOLUTION_FOCUSED":
        return route_to_solution_synthesis()
    else:  # INFORMATIONAL
        return comprehensive_information_synthesis()
```

---

## 📂 File Structure
```
collabsearch/
├── src/
│   ├── disambiguation/
│   ├── expert_analysis/
│   ├── smart_routing/
│   ├── rag_enhancement/
│   └── synthesis/
├── evaluation/
│   ├── user_study_data/
│   ├── questionnaires/
│   └── analysis_scripts/
├── notebooks/
└── requirements.txt
```

---

## 🤝 Contributing
1. Fork the repository  
2. Create a feature branch:  
   ```bash
   git checkout -b feature/enhancement
   ```  
3. Commit changes:  
   ```bash
   git commit -am 'Add enhancement'
   ```  
4. Push to branch:  
   ```bash
   git push origin feature/enhancement
   ```  
5. Create a Pull Request  

---

## 📖 Citation
```bibtex
@mastersthesis{cedeno2025collabsearch,
  title={CollabSearch: LLaMA as Collaborative Agent for Search Tasks},
  author={Cedeno Batista, Gloris Denisse},
  year={2025},
  school={University of Glasgow, School of Computing Science},
  type={MSc Dissertation}
}
```

---

## 📜 License
This project is part of academic research conducted at the **University of Glasgow, School of Computing Science**.  

---

## 🙏 Acknowledgments
- **Supervisor:** Joemon Jose, University of Glasgow  
- **Funding:** National Secretary of Science, Technology, and Innovation of Panama  
- **Research Context:** MSc Computer Science project, University of Glasgow  
