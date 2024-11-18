# LLM-Data-Engineering
**Overview**
This repository contains a complete solution for ingesting, processing, vectorizing, and querying mixed structured and unstructured data. The pipeline also integrates Retriever-Augmented Generation (RAG) to generate summaries from queried data. The project demonstrates scalable and efficient data engineering practices using modern NLP tools and vector storage.

**Features**
**Data Ingestion:**
1. Load data from SQLite database and CSV file.
2. Ensure schema is optimized for querying.
   
**Data Preprocessing:**
1. Clean text data by removing noise.
2. Handle missing values for robust analysis.
   
**Text Embedding:**
1. Use sentence-transformers to generate embeddings for unstructured text.
2. Support batch processing for large datasets.
   
**Similarity Search:**
1. Implement FAISS for efficient similarity-based search.

**RAG Integration:**
1. Generate concise summaries for retrieved data using pre-trained transformer models.

**Logging and Monitoring:**
1. Track data pipeline performance and execution time for key stages.
   
**Scalability:**
1. Batch processing and modular design enable handling large datasets.
