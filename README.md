# 🧠 Multilingual Retrieval-Augmented Diabetes Assistant

A multilingual, retrieval-grounded healthcare assistant designed to provide **evidence-based diabetes information** using trusted medical sources and large language models.  
The system focuses on **reducing hallucinations**, supporting **personalized responses**, and enabling **safe, medically grounded AI interactions**.

---

## 📌 Motivation

Diabetes management requires continuous access to reliable, understandable medical guidance. While large language models can generate natural responses, they may produce hallucinated or non-evidence-based medical information.

This project explores how **Retrieval-Augmented Generation (RAG)** can improve factual reliability by grounding responses in trusted medical guidelines.

---

## 🎯 Project Goals

- Provide grounded diabetes-related responses using trusted medical sources  
- Support multilingual interaction (English + Spanish)  
- Incorporate patient context for personalization  
- Reduce hallucination risk using retrieval-based grounding  
- Evaluate healthcare LLM responses using semantic metrics  

---

## 🏗️ System Architecture

### Pipeline Overview
User Query
↓
Language Detection
↓
Sentence Embedding (MiniLM)
↓
Vector Search (FAISS)
↓
Medical Knowledge Retrieval (WHO / ADA / CDC / NDEP)
↓
Context Injection into LLM (LLaMA-based)
↓
Personalized Response Generation


---

## 📚 Knowledge Sources

- WHO Diabetes Guidelines  
- CDC Diabetes Resources  
- ADA Clinical Guidance  
- NDEP Public Education Material  
- MedQuAD Medical QA Dataset  

Only trusted public-health sources were used to improve factual grounding.

---

## 🌍 Multilingual Support

The system supports:
- English queries  
- Spanish queries (via translation + retrieval + response generation pipeline)

---

## 👤 Personalization Layer

User profiles may include:
- Demographics  
- Medical history  
- Medication information  
- Symptom context  

Used to generate context-aware responses while maintaining safety boundaries.

---

## 📊 Evaluation

The system was evaluated using both lexical and semantic metrics.

| Metric | Purpose |
|---|---|
| BLEU | Exact phrase matching |
| ROUGE | Word overlap and recall |
| METEOR | Synonym-aware similarity |
| BERTScore | Semantic meaning similarity |

### Key Results

| Dataset | BLEU-4 | ROUGE-1 | ROUGE-L | METEOR | BERTScore |
|---|---|---|---|---|---|
| English | 0.024 | 0.153 | 0.138 | 0.315 | **0.865** |
| Spanish | 0.015 | 0.165 | 0.127 | 0.282 | **0.70** |

Semantic metrics (BERTScore) showed strong meaning preservation even when lexical overlap was low, which is expected for LLM-based healthcare QA.

---

## 🛡️ Trustworthy AI Considerations

This project explores:

- Retrieval grounding to reduce hallucinations  
- Use of trusted medical knowledge sources  
- Multilingual fairness considerations  
- Evaluation beyond lexical similarity  
- Responsible response framing (non-diagnostic)

---

## ⚠️ Limitations

- Not connected to real patient EHR data  
- No formal clinical validation (research prototype only)  
- Limited multilingual medical dataset coverage  
- No calibrated uncertainty scoring yet  

---

## 🔬 Future Work

- Uncertainty estimation and confidence calibration  
- EHR integration (with privacy safeguards)  
- Clinician-in-the-loop evaluation  
- Expansion to broader metabolic disease support  
- Digital twin style patient state modeling  

---

## 🧪 Tech Stack

- Python  
- FAISS (Vector Search)  
- SentenceTransformers (MiniLM Embeddings)  
- LLaMA-based LLM  
- Streamlit (Interface)  
- Scikit-learn (Supporting ML components)

---

## ❗ Disclaimer

This system is for **research and educational purposes only**.  
It is **not intended for medical diagnosis or treatment decisions**.  
Users should always consult qualified healthcare professionals.

---

## 👩‍💻 Author

**Kanika Saxena**  
M.S. Computer Science — University at Buffalo  

Focus Areas:
- Trustworthy AI  
- Healthcare Machine Learning  
- Digital Twins  
- Applied Machine Learning Systems  

---

## 🧭 Research Direction

This project motivated interest in:
- Trustworthy AI for healthcare systems  
- Uncertainty-aware ML  
- Retrieval-grounded medical LLMs  
- Digital twin style modeling of patient state  
- Safe deployment of AI in high-stakes environments


