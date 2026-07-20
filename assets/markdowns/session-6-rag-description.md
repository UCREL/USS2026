## Session 6: Building a Basic RAG System

**Facilitator:** Dr Hansi Hettiarachchi  
**Repository:** [UCREL/Session-6-RAG-USS-2026](https://github.com/UCREL/Session-6-RAG-USS-2026)  
**Notebook:** [Open the practical notebook in Google Colab](https://colab.research.google.com/github/UCREL/Session-6-RAG-USS-2026/blob/main/Session_6_Building_a_Basic_RAG_System.ipynb)

This hands-on session introduces the core components of a **Retrieval-Augmented Generation (RAG)** pipeline. Participants will build a complete, transparent RAG system from first principles rather than relying on an all-in-one framework.

The practical uses the labelled **PubMedQA** dataset, which contains 1,000 biomedical research questions paired with relevant paper abstracts, expert-written answers and `yes`, `no` or `maybe` decisions. The task demonstrates how retrieval can ground an LLM's response in published evidence and support answers with traceable citations.

### What the notebook covers

The notebook guides participants through:

1. setting up the required open-source libraries;
2. loading and inspecting the PubMedQA corpus;
3. splitting documents into overlapping text chunks;
4. generating sentence embeddings and building a FAISS vector index;
5. implementing and comparing:
   - dense semantic retrieval;
   - lexical BM25 retrieval; and
   - hybrid retrieval;
6. evaluating retrieval using metrics such as **Recall@k** and **MRR@k**;
7. constructing a grounded prompt that requires evidence-based answers, citations and appropriate abstention;
8. generating answers with a small open-weight instruction-tuned language model;
9. evaluating end-to-end responses against reference answers and verdicts; and
10. examining common RAG failure modes and considerations for production systems.

### Learning outcomes

By the end of the session, participants should be able to:

- transform a raw corpus into a chunked, embedded and searchable index;
- explain the differences between dense, lexical and hybrid retrieval;
- construct prompts that constrain an LLM to retrieved evidence;
- evaluate both retrieval quality and generated answers;
- identify common RAG failure modes and select appropriate improvements; and
- understand how a basic experimental RAG pipeline relates to a larger production architecture.

### Main technologies

The notebook uses:

- `datasets` for loading PubMedQA;
- `sentence-transformers` for text embeddings;
- `faiss-cpu` for dense vector search;
- `rank_bm25` for lexical retrieval;
- `transformers` for local text generation; and
- `accelerate` for efficient model placement and execution.

All components are open source, and the notebook does not require a commercial API key.

### Running the practical

The notebook can run on a CPU, but a Google Colab **T4 GPU** is recommended for faster generation:

`Runtime → Change runtime type → T4 GPU`

Cells labelled **🧪 Activity** contain participant exercises. Cells labelled **⏭️ Optional** may be skipped when time is limited.
