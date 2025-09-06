# RAG Embedding Indexing Comparison

This project explores indexing strategies for vector databases using **FAISS** (local) and **Pinecone** (cloud).  
It is part of an assignment on **Advanced Topics in Retrieval-Augmented Generation (RAG)**.

## 🚀 Tasks
1. **Flat Index (Exact Search)** – Baseline using FAISS & Pinecone.
2. **Dimensionality Reduction (PCA)** – Reduce embedding size for efficiency.
3. **Optimized Index (HNSW)** – Approximate nearest neighbor for faster queries.
4. **Evaluation** – Compare indexing time and memory usage.

## 📊 Results
| Task             | FAISS Time (s) | FAISS Mem (MB) | Pinecone Time (s) | Pinecone Mem (MB) |
|------------------|----------------|----------------|-------------------|-------------------|
| Flat (Exact)     | 0.0015         | 0.0000         | 6.1179            | 0.8110            |
| Reduced Dim      | 0.0009         | 0.0000         | 2.8372            | 0.2703            |
| Optimized (HNSW) | 0.1182         | 0.0000         | 5.1221            | 0.0000            |

📈 See `/results/` for plots of **indexing time** and **memory usage**.

## 🛠️ Setup
```bash
pip install -r requirements.txt
