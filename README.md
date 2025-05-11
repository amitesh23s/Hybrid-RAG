# 🧠 Hybrid Graph RAG vs Traditional RAG Evaluation

This project implements and evaluates a Hybrid Graph-based Retrieval-Augmented Generation (RAG) system in comparison with a Traditional RAG pipeline using LTIMindtree's partnership dataset. The evaluation is conducted using a language model as a judge across four qualitative metrics.

---

## 🚀 Getting Started

Follow the steps below to set up and run the project end-to-end.

---

## 📦 Prerequisites

- Docker
- Python 3.8 or higher
- `pip` package manager
- Jupyter Notebook

---

## ⚙️ Setup Instructions

### 1. Install Docker

Install Docker from the [official Docker website](https://www.docker.com/get-started/) and ensure it's running on your machine.

### 2. Start Services with Docker

Navigate to the project directory and run:

```bash
docker-compose up
```

### 3. Set Up Python Virtual Environment
python -m venv venv
source venv/bin/activate  # For macOS/Linux
  OR
venv\Scripts\activate     # For Windows

### 4. Install Required Dependencies
pip install -r requirements.txt

### 5. Add Your OpenAI API Key
OPENAI_API_KEY=your_openai_api_key_here


---

### Run the following notebooks in order:
- `ml_project.ipynb` (for Hybrid Graph RAG implementation)
- `traditional_rag.ipynb` (for Traditional RAG baseline)
- `comparison.ipynb` (for answer evaluation and metrics visualization)

---

## 📊 Evaluation Metrics

We evaluate each answer across the following four dimensions:

- **Comprehensiveness**: How thoroughly the answer covers all aspects of the question.
- **Diversity**: The variety and richness of insights and perspectives presented.
- **Empowerment**: How well the answer helps users make informed judgments.
- **Directness**: The clarity and specificity with which the answer addresses the question.

An LLM evaluator performs head-to-head comparisons of generated answers to determine which system (Hybrid RAG or Traditional RAG) performs better under each metric.

---

## 📈 Results Summary

A bar chart is generated to illustrate the number of wins by each method (Hybrid RAG, Naive RAG, or Tie) across the evaluation categories. This helps visualize where each method excels and highlights the impact of integrating graph-based context into retrieval.

### Project structure
  - ml_project.ipynb             # Hybrid Graph RAG implementation
  - traditional_rag.ipynb        # Traditional RAG pipeline
  - comparison.ipynb             # LLM-based evaluation and metrics visualization
  - requirements.txt             # Python dependencies
  - docker-compose.yml           # Vector DB / Graph DB configuration
  - .env                         # User-created file with OpenAI API key
  - README.md                    # Instructions and project summary
