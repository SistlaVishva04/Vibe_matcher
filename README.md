# 🧥 Vibe Matcher — AI Fashion Recommender  

### 🔹 Overview  
**Vibe Matcher** is a mini AI-powered recommendation system that connects users’ *vibe-based queries* (like “urban chic” or “cozy winter feel”) with fashion products that best match their mood and aesthetic.  
Built using **sentence embeddings** and **cosine similarity**, this notebook demonstrates how AI can interpret *style language* and translate it into meaningful product matches.  

---

## 🚀 Features
- 🧠 **Semantic Understanding:** Uses embeddings (`all-MiniLM-L6-v2`) to capture contextual meaning of descriptions and vibes.  
- 🎯 **Vibe Query Matching:** Finds top-3 products that align with a user’s mood or style.  
- ⚡ **Fast & Lightweight:** Works locally or in Google Colab under 0.03s per query.  
- 📊 **Evaluation Dashboard:** Measures query latency and similarity performance.  
- 💡 **Extendable:** Can easily integrate with Pinecone or FAISS for scalable vector search.

---

## 🧩 Project Workflow

| Step | Description | Output |
|------|--------------|---------|
| **1. Data Prep** | Created a dataset of 15 fashion products with `name`, `desc`, and `vibes`. | `vibe_matcher_fashion_dataset.csv` |
| **2. Embeddings** | Generated text embeddings using Sentence Transformers (`all-MiniLM-L6-v2`). | `vibe_matcher_embedded.csv` |
| **3. Vector Search** | Used cosine similarity to find top-3 similar products for a vibe query. | Printed ranked results |
| **4. Evaluation** | Measured latency & similarity for 4 test queries. | Performance table + chart |
| **5. Reflection** | Identified improvements and next steps. | Final summary |

---

## 🧠 Example Query Results

| Query | Top Match | Similarity |
|--------|------------|-------------|
| energetic urban chic | Street Hoodie | 0.44 |
| cozy warm winter | Cozy Sweater | 0.57 |
| tropical vacation beach vibes | Beach Shorts | 0.63 |
| luxury elegant evening wear | Silk Scarf | 0.66 |

---

## ⚙️ Tech Stack
- **Python 3.10+**  
- **Pandas** — Data handling  
- **Sentence Transformers** — Embedding generation  
- **scikit-learn** — Cosine similarity  
- **Matplotlib** — Latency visualization  
- **Google Colab** — Execution environment  

---

## 📊 Performance Metrics

| Metric | Result |
|---------|--------|
| Avg Query Latency | 0.02 sec |
| Avg Similarity (Top-3) | 0.48 |
| Good Match Threshold (>0.7) | 0 |
| Dataset Size | 15 products |

---

## 🔍 Reflection
1. Combined descriptions and vibe tags improved contextual relevance.  
2. Current similarity scores suggest richer descriptions could enhance semantic matching.  
3. Integration with **Pinecone** or **FAISS** would improve scalability.  
4. Latency under 30ms shows real-time recommendation is feasible.  
5. Future improvements: multimodal embeddings (image + text) and adaptive personalization.

---

## 🧭 Why AI at Nexora?
> At **Nexora**, AI is the creative core of personalization. The Vibe Matcher prototype showcases how semantic intelligence can bridge emotion and aesthetics — turning user moods into meaningful fashion matches. This reflects Nexora’s mission to humanize digital experiences through adaptive AI systems.  

---

## 🧰 How to Run

### 🔸 In Google Colab
1. Upload `vibe_matcher_fashion_dataset.csv`  
2. Run notebook cells in order  
3. Output: top-3 vibe matches for each query + performance chart  

### 🔸 In Local Environment
```bash
pip install pandas sentence-transformers scikit-learn matplotlib
python vibe_matcher_notebook.ipynb
