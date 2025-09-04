
A2: Evaluation of RAG Models

## 🎯 Objective
Assess the quality and efficiency of **Retrieval-Augmented Generation (RAG)** systems.

## 📝 Tasks Completed
1. Defined evaluation metrics for RAG:
   - **Relevance:** Precision@k, Recall@k
   - **Faithfulness:** Hallucination rate
   - **Response Quality:** BLEU, ROUGE
2. Compared two systems:
   - **Pure LLM:** Flan-T5 without retrieval.
   - **RAG-enabled LLM:** Flan-T5 + FAISS retrieval.
3. Implemented runtime Q&A loop where the user can:
   - Ask questions.
   - Get answers from both systems.
   - See evaluation metrics automatically after each query.
4. Stored results and provided **graphical comparison** between RAG and Pure LLM for multiple queries.

## ⚙️ Setup
Clone the repository and install dependencies:

```bash
git clone https://github.com/your-username/your-repo-name.git
cd A2_evaluation_RAG
pip install -r requirements.txt
