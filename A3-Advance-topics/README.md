# Assignment 3: Advanced Topics in RAG

This repository contains experiments for **Advanced Topics in Retrieval-Augmented Generation (RAG)**.  
Three tasks are implemented in Python, and the fourth task (literature review) is briefly explained below.

---

## 🚀 Tasks Implemented

### **Task 1: Maximum Marginal Relevance (MMR)**
- **Goal:** Improve retrieval results by avoiding redundancy.  
- **How it works:**  
  - Computes similarity between query and documents.  
  - Iteratively selects documents that are **relevant** to the query but also **different** from already chosen docs.  
  - Controlled by a diversity parameter (0 = relevance only, 1 = diversity only).  
- **Benefit:** Ensures top results cover multiple aspects of the query instead of repeating the same idea.

- 
### **Task 2: Self Querying Retriever**
- **Goal:** Make queries smarter by rewriting or expanding them with an LLM.
- **How it works:**
  - User’s raw query → passed through a small LLM (flan-t5-small).
  - The LLM outputs an enhanced query with synonyms and related terms.
  - Retrieval then uses this expanded query to fetch richer results.
- **Example:**
  - Query: “Tell me about Paris.”
  - Enhanced: “Paris, France, Eiffel Tower, Louvre, French history”
  - Challenge: Small LLMs sometimes hallucinate (e.g., “Paris, New York”), which shows a real limitation in RAG systems.

### **Task 3: Hybrid Retrieval (Keyword + Embeddings)**
- **Goal:** Combine the strengths of keyword search (precision) and semantic embeddings (recall).
- **How it works:**
  - Keyword search (TF-IDF): Finds documents with exact word matches.
  - Embedding search (Sentence-BERT): Finds semantically similar documents.
  - Hybrid score: Weighted combination of both methods.
- **Benefit: **Produces more balanced results → precise but also covers synonyms/related terms.

### **Task 4: Literature Review (Challenges in RAG)**
Although not implemented in this repo, Task 4 explores current challenges in RAG systems:
- **Hallucinations:**
  - LLMs sometimes generate information not supported by retrieved documents.
  - Challenge: grounding answers strictly in retrieved evidence.
- **Latency:**
  - Retrieval + generation makes responses slower compared to vanilla LLMs.
  - Challenge: optimizing pipelines for real-time use.
- **Memory:**
  - Handling long conversations or large document sets exceeds context windows.
  - Challenge: efficient long-term memory mechanisms.
- **Ongoing Research:**
  - Techniques like re-ranking (MMR), query rewriting, hybrid search, and memory-efficient architectures are being explored to address these problems.

- **Run:**
  ```bash
  python A3-of-RAG.ipynb

